# CI incident containment — 2026-10-09

Repository: `ThreeAndTwo/anchor`
Branch: `clean-up-parse-account-function`
Inspected head: `aeafc798a52fbe890457a3a8899e9f4a28cfb751`

Actions were disabled before this cleanup. Keep them disabled until the repository owner explicitly approves restoration.

The owner confirmed that this personal repository must not contain GitHub Actions workflows. This change removes every file under `.github/workflows` on this branch, regardless of its name.

Files removed in this change:

- `.github/workflows/no-cashing-tests.yaml` — original Git object `f5a0c920fc4f79c4e63fbcb88839f674591d8991`.
- `.github/workflows/tests.yaml` — original Git object `2e5a12e5d1472af8f456c6dbb87396101b59fe99`.

Evidence and limits

- Unauthorized workflows were observed attempting credential or repository-history disclosure. A successful workflow run alone does not prove data receipt or credential validity.
- Existing Git history is retained as evidence. No release, tag, force push, or history rewrite is part of this cleanup.
- Revoking a GitHub token does not rotate credentials issued by other services.
- The initial credential compromise and the authentication method used for the mass write remain under investigation.
- This record supersedes any earlier note suggesting that personal-repository workflows should be retained.
