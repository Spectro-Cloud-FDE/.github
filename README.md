# .github

Default community-health files for the Spectro-Cloud-FDE organization.
GitHub applies these to every repo in the org that doesn't define its own.

**This repository is public.** Never put customer names, internal URLs or
engagement details here — those belong in `.github-private` or `fde-meta`.

It also hosts the org's **reusable workflows** (they contain no secrets):

```yaml
jobs:
  secret-scan:
    uses: Spectro-Cloud-FDE/.github/.github/workflows/secret-scan.yml@main
  lint:
    uses: Spectro-Cloud-FDE/.github/.github/workflows/lint.yml@main
    with: { shellcheck: true, terraform-fmt: false, yamllint: false }
```
