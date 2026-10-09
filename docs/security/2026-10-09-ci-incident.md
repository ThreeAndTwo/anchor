# CI incident containment — 2026-10-09

Repository: `ThreeAndTwo/anchor`
Branch: `add_versioned_transactions`
Inspected head: `b20b5dabb1c1be58c4d8ecc439da2c1ad93c29d6`

Actions were disabled before this cleanup. Keep them disabled until the repository owner explicitly approves restoration.

The owner confirmed that this personal repository must not contain GitHub Actions workflows. This change removes every file under `.github/workflows` on this branch, regardless of its name.

Files removed in this change:

- `.github/workflows/no-caching-tests.yaml` — original Git object `4a8a663aca25ce04cb6dc808845eea50c01ba920`.
- `.github/workflows/reusable-tests.yaml` — original Git object `24e616b2133e896bc92a41f053e56473cbcb9968`.
- `.github/workflows/tests.yaml` — original Git object `d3b8e977090827210e72be02faa4337b3a34acc4`.

Evidence and limits

- Unauthorized workflows were observed attempting credential or repository-history disclosure. A successful workflow run alone does not prove data receipt or credential validity.
- Existing Git history is retained as evidence. No release, tag, force push, or history rewrite is part of this cleanup.
- Revoking a GitHub token does not rotate credentials issued by other services.
- The initial credential compromise and the authentication method used for the mass write remain under investigation.
- This record supersedes any earlier note suggesting that personal-repository workflows should be retained.
