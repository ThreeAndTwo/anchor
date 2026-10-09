# CI incident containment — 2026-10-09

Repository: `ThreeAndTwo/anchor`
Branch: `master`
Inspected head: `a87c8c25403c2a7434078a9a254d381fcb9964a3`

Actions were disabled before this cleanup. Keep them disabled until the repository owner explicitly approves restoration.

The owner confirmed that this personal repository must not contain GitHub Actions workflows. This change removes every file under `.github/workflows` on this branch, regardless of its name.

Files removed in this change:

- `.github/workflows/no-caching-tests.yaml` — original Git object `bb997e91b5c1d4074524c58b65c41bc8cc1869ee`.
- `.github/workflows/reusable-tests.yaml` — original Git object `bf2019f8b4ff98cd65060672d8f342df0665eba9`.
- `.github/workflows/tests.yaml` — original Git object `870b2acea717ce55dfb0b1748ac891a0ef8e18d7`.

Evidence and limits

- Unauthorized workflows were observed attempting credential or repository-history disclosure. A successful workflow run alone does not prove data receipt or credential validity.
- Existing Git history is retained as evidence. No release, tag, force push, or history rewrite is part of this cleanup.
- Revoking a GitHub token does not rotate credentials issued by other services.
- The initial credential compromise and the authentication method used for the mass write remain under investigation.
- This record supersedes any earlier note suggesting that personal-repository workflows should be retained.
