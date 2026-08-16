# AI-assisted private rebaselining: a gentle Git workflow for Ī-puāwai

**Purpose:** This note records a deliberate, low-risk way to begin rebaselining a locally developed Flask/SQLite application while learning Git step by step. It is written for a development workflow where the **Ī-puāwai app repository remains private and local**, while the separate **Manifesting IUWE Living Book** may publish the lessons, methods, and non-sensitive documentation.

> **Boundary:** The application repository is not pushed to GitHub. Only a documentation file in the Living Book repository is committed and pushed.

## Why start this way

A rebaseline can feel risky because it touches identity, data, source material, and application architecture at the same time. The safer pattern is to make the project’s current state observable first, preserve an evidence copy, make one small change at a time, verify it, and only then create a local Git checkpoint.

This approach is intentionally suitable for a lean Windows 10 development computer. It does not require Docker, a cloud database, a large test suite, a background service, or a duplicate media collection. Resource-intensive image research and development can remain on a separate computer; the development repository exchanges only compact manifests, hashes, decisions, and file references when the time comes.

## Two repositories, two different purposes

| Repository | Example local path | Purpose | GitHub rule |
|---|---|---|---|
| Ī-puāwai application | `C:\ipuawai` | Private Flask, SQLite, seed, and development work. | **No push to GitHub.** |
| Manifesting IUWE Living Book | `C:\ipuawai_manifest` | Public/non-sensitive architecture notes, methods, and documentation. | Commit and push documentation only after review. |

Never run an application-repository command in the Living Book repository, and never publish database copies, `.env` files, credentials, source datasets that should remain private, media collections, or application code merely because a documentation note is being published.

## Stage 0: establish evidence before changing anything

The first objective is not to fix code. It is to preserve the exact starting point so that every later decision is explainable and reversible.

### 0.1 Confirm the correct repository

Open PowerShell in the **application** repository and run read-only Git checks:

```powershell
Set-Location 'C:\ipuawai'
git rev-parse --show-toplevel
git status --short
git branch --show-current
git log -1 --oneline
```

These commands answer four practical questions: “Am I in the right repository?”, “What has not yet been saved in Git?”, “Which branch am I on?”, and “What is the latest committed checkpoint?” They do not modify any file, create a commit, or contact GitHub.

> Do not use `git reset`, `git clean`, `git stash`, `git add`, `git commit`, or `git push` merely to make a status display look tidy. Uncommitted work is information, not a failure.

### 0.2 Create a local-only working branch

A branch is a named local line of work. It does not publish anything. It gives the rebaselining work a home without disturbing the prior `main` checkpoint.

```powershell
Set-Location 'C:\ipuawai'
$branch = 'chore/ipuawai-rebaseline-stage0'

if (git show-ref --verify --quiet "refs/heads/$branch") {
    git switch $branch
} else {
    git switch -c $branch
}

git branch --show-current
git status --short
```

The existing modified and untracked files should remain visible after the branch switch. That is expected: creating a branch does not erase, stage, commit, or upload local work.

### 0.3 Capture an evidence snapshot

The evidence snapshot records Git state, hashes the lean source/seed inputs, and copies the legacy SQLite database. The database copy is verified by SHA-256 and marked read-only. The original remains in place.

The inventory excludes resource-heavy and sensitive paths, such as virtual environments, media collections, uploads, audio collections, OpenMoji/static image collections, `.git`, and `.env` values.

```powershell
Set-Location 'C:\ipuawai'
$stamp = Get-Date -Format 'yyyyMMdd-HHmmss'
$evidence = Join-Path $PWD ("evidence\stage-0\$stamp")
New-Item -ItemType Directory -Force $evidence | Out-Null

# Record Git evidence without changing history.
git rev-parse --show-toplevel | Set-Content -Encoding utf8 (Join-Path $evidence 'repository_root.txt')
git branch --show-current | Set-Content -Encoding utf8 (Join-Path $evidence 'branch.txt')
git log -1 --oneline | Set-Content -Encoding utf8 (Join-Path $evidence 'head_commit.txt')
git status --porcelain=v1 -uall | Set-Content -Encoding utf8 (Join-Path $evidence 'git_status_before.txt')
git diff --binary | Set-Content -Encoding utf8 (Join-Path $evidence 'tracked_changes_before.patch')

# Copy and verify the legacy database. Close the running app/DB tools first.
$legacyDb = Join-Path $PWD 'ipuawai.db'
$legacyCopy = Join-Path $evidence ("ipuawai_legacy_{0}.db" -f $stamp)
$originalHash = (Get-FileHash $legacyDb -Algorithm SHA256).Hash
Copy-Item -LiteralPath $legacyDb -Destination $legacyCopy -ErrorAction Stop
$copyHash = (Get-FileHash $legacyCopy -Algorithm SHA256).Hash
if ($originalHash -ne $copyHash) { throw 'Database copy hash mismatch — stop.' }
Set-ItemProperty -LiteralPath $legacyCopy -Name IsReadOnly -Value $true
```

A good Stage 0 evidence folder includes the branch, starting commit, status record, tracked-change patch, hash inventory, database copy, and a small JSON manifest. This is a local rollback/evidence aid. It is not automatically a Git commit and it is not a public upload.

## Stage 1: make one small, testable foundation change

Once the state is preserved, change one isolated component at a time. The first Ī-puāwai foundation is an identity helper that does not need to open the database or change a Flask route.

### 1.1 Stable UUID and public-reference helper

A new `app\identity.py` module can provide one generation path for future seeders, migrations, and services.

| Concept | Rule |
|---|---|
| UUID | Stable internal identifier. Generate once, preserve forever. Prefer UUIDv7 when the Python runtime supports it; otherwise use UUIDv4. |
| Public reference | Stable human-facing handle, for example `w-HYJN3AAJ`. |
| Prefix | One to three lowercase letters. `w` means word; `ws` means word sense; `ph` means phrase; `pe` means practice event; `se` means scheduled event. |
| Random suffix | Uses a safe alphabet that excludes visually confusing characters. |
| Never derive identity from | A word, translation, filename, source row, category, curriculum order, asset path, Discourse URL, tag, or topic number. |

The helper is deliberately database-independent first. A later migration adds a global case-insensitive identity registry and collision checking. This keeps the earliest test fast and understandable on a modest development machine.

### 1.2 SQLite foreign-key protection

SQLite accepts foreign-key declarations but does not enforce them unless each connection enables `PRAGMA foreign_keys=ON`. A small SQLAlchemy connection listener in `app\extensions.py` enables this for every SQLite connection created by the app.

This safeguard prevents new broken relationships in the clean baseline. It does not rewrite, delete, or conceal historic data issues in the evidence database.

### 1.3 Lean test harness

A standard-library `unittest` harness is sufficient at the beginning. It should prove that the identity helper creates a valid UUID, formats a safe public reference, validates prefixes, retries a simulated collision, and fails explicitly when no unique reference can be found. A small in-memory SQLite test should prove foreign-key enforcement.

The important discipline is simple:

```text
one isolated change → syntax check → focused test → inspect git diff → decide whether to commit
```

## Future rebaseline stages

The small foundation changes prepare, but do not perform, later work.

| Later stage | What it will add | What it will not do automatically |
|---|---|---|
| Identity-aware clean schema | UUID/public-reference fields, registry, language/dialect tables, source memberships, word senses, Discourse staging. | Replace the active database. |
| Provenance-aware word seed | One canonical English word plus preserved Kākano, Dolch, and Papawai source occurrences. | Edit source CSV files or treat overlap as an error. |
| Bilingual relation proof | Separate English and Māori word/sense records, then a reviewed `te ↔ the` relation. | Infer language approval or translation from topic titles. |
| Discourse staging | External community/topic records keyed by `(community, topic_id)`. | Treat a URL, topic title, tag, or attachment as local identity. |
| Asset description ingestion | Reviewable caption records attached to a real asset UUID and provenance path. | Re-caption, rename, or reprocess the Eagle/Unsplash collection during rebaselining. |
| Kākano expansion | Add the approved untouched 144-row source artifact. | Change the existing 42-row source evidence. |
| Word-to-image matching | Explicit source/family/variant links and a thumbnail review workflow. | Infer asset identity from filenames or visual appearance alone. |

## Local checkpoints and public documentation

A Git branch is not a Git commit. A commit is a named, recoverable local checkpoint. A push copies committed history to a configured remote such as GitHub.

For the private application repository, the safe rule is:

```text
Inspect → test → inspect diff → choose a small local commit only if approved → do not push.
```

For the separate Living Book repository, a public documentation change can be committed and pushed when it contains only non-sensitive explanatory material.

## Publishing this note from the Living Book repository

Save this file in the Living Book repository at:

```text
08-our-i-puawai/01-identity-and-provenance/ai-assisted-private-rebaselining-workflow.md
```

Then use the following commands from the **Living Book** repository, not from `C:\ipuawai`:

```powershell
Set-Location 'C:\ipuawai_manifest'

# Check the correct repository and its current state.
git rev-parse --show-toplevel
git branch --show-current
git status --short

# Review only the documentation file that will be published.
git add -- '08-our-i-puawai/01-identity-and-provenance/ai-assisted-private-rebaselining-workflow.md'
git diff --cached -- '08-our-i-puawai/01-identity-and-provenance/ai-assisted-private-rebaselining-workflow.md'

# Make one documentation-only local checkpoint.
git commit -m "docs(i-puawai): add private rebaselining workflow"

# Verify the commit and then publish this Living Book documentation only.
git status --short
git log -1 --oneline
git push origin main
```

Before the final `git push`, stop and confirm that the staged diff contains only this Markdown document and no secret, database, application, media, credential, or unrelated file.

## What this workflow teaches

This paced approach turns Git into a practical safety tool rather than an obstacle:

| Git command | Meaning in plain language |
|---|---|
| `git status --short` | “What files are changed or new, but not yet in a commit?” |
| `git switch -c <branch>` | “Create a local named lane for this work.” |
| `git diff` | “Show exactly what changed in tracked files.” |
| `git add -- <file>` | “Select this exact reviewed file for the next commit.” |
| `git diff --cached` | “Show exactly what the next commit will contain.” |
| `git commit -m "…"` | “Create a named local restore point.” |
| `git push origin main` | “Publish already committed history to the remote.” |

The decisive safeguard is not a single command. It is the habit of checking the repository, preserving evidence, limiting each change, testing it, reviewing the diff, and only then deciding whether to commit or publish.
