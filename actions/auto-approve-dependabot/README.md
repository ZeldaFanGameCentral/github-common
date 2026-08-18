# auto-approve-dependabot

Approves dependabot PRs and enables auto-merge, if the workflow is triggered by dependabot.

## Inputs

### `github-token`

**Required:** false

**Default:** `${{ github.token }}`

## Outputs

None

## Permissions

**Required:** `contents: write` (needed by `gh pr merge`)

**Required:** `pull-requests: write`

> [!NOTE]
> Dependabot-triggered runs get a read-only `GITHUB_TOKEN` unless
> Settings > Actions > `Allow GitHub Actions to create and approve pull requests`
> is enabled. Squash merging must also be enabled on the consuming repo.
