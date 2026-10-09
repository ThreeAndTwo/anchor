# CI incident containment — 2026-10-09

Repository: `ThreeAndTwo/anchor`
Branch: `update-web3`
Inspected head: `4b007fb730d633392c8a0d1fdfedfb86ed3e5af6`

Actions were disabled before this cleanup. Keep them disabled until the repository owner explicitly approves restoration.

The owner confirmed that this personal repository must not contain GitHub Actions workflows. This change removes every file under `.github/workflows` on this branch, regardless of its name.

Files removed in this change:

- `.github/workflows/no-caching-tests.yaml` — original Git object `c87e985de89d9e7b49457b90dbd02dbc72667fc9`.
- `.github/workflows/reusable-tests.yaml` — original Git object `24e616b2133e896bc92a41f053e56473cbcb9968`.
- `.github/workflows/tests.yaml` — original Git object `9bcdb0401fa711050eccbc1ca9a1df3071e8948e`.

Evidence and limits

- Unauthorized workflows were observed attempting credential or repository-history disclosure. A successful workflow run alone does not prove data receipt or credential validity.
- Existing Git history is retained as evidence. No release, tag, force push, or history rewrite is part of this cleanup.
- Revoking a GitHub token does not rotate credentials issued by other services.
- The initial credential compromise and the authentication method used for the mass write remain under investigation.
- This record supersedes any earlier note suggesting that personal-repository workflows should be retained.
