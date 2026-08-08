# Contributing

These are the org-wide defaults. A repo that ships its own `CONTRIBUTING.md` overrides this one, so
read the repo first.

## Before you start

Check the default branch. It is `master` on some repos and `main` on others. Branch from the remote,
not from whatever your working copy happens to be holding.

```bash
git fetch origin
git switch -c feat/<short-slug> origin/<default-branch>
```

Several people and several agents run in parallel across these repos. Use one branch per unit of
work, and use a `git worktree` when you need more than one going at once. A stale local checkout is
the most common cause of a merge that looks clean and is not.

## Branches

`feat/<slug>` for features, `fix/<slug>` for fixes, `docs/<slug>` for documentation, `chore/<slug>`
for everything else. Keep the slug short and specific. `feat/run-health-gate` beats `feat/updates`.

## Commits

Conventional Commits.

```
type(scope): imperative subject
```

`type` is one of `feat`, `fix`, `docs`, `chore`, `refactor`, `test`, `ci`, `perf`. Keep the subject
under 72 characters and write it as a command. Explain why in the body when the change is not
obvious from the diff.

## Pull requests

One PR, one concern. If you cannot describe it in a sentence, split it.

Fill in the template. The part that matters is how you verified the change, and "CI is green" is not
verification on its own. Say what you ran and what you saw.

Draft PRs are welcome and encouraged early. Mark it ready when CI passes and the description is
accurate.

Stacked PRs need care. A PR targeting another PR's branch does not always get the checks you expect,
and merging the parent rewrites what the child is diffing against. Rebase the child after the parent
lands, then confirm CI actually ran.

## CI

Most repos expose a single aggregate status check as the required gate. It runs on every pull
request. Individual jobs may skip on path filters, but the aggregate always reports, which is what
keeps a fully skipped workflow from silently satisfying branch protection.

If CI is red, fix it. Do not merge around it and do not disable the check. If the failure is
inherited from the default branch rather than caused by your change, say so in the PR and link the
run.

## Tests

A test that passes before your fix proves nothing. Revert the fix, confirm the test fails, restore
the fix, confirm it passes. Then you know what it covers.

Add tests for the branch you actually changed, including the error path. A read that fails must not
render as an empty success.

## Database changes

Migrations are append-only and numbered. Claim your number, regenerate any manifest the repo keeps,
and never edit a migration that has already run somewhere. Number collisions between parallel
branches are common, so re-check yours right before you merge.

## Secrets

Never commit a credential. Not in code, not in a test fixture, not in a commit message, and not in a
screenshot. Secret scanning and push protection are on, so a push carrying one gets blocked.

If you push a secret by accident, treat it as leaked. Rotate it first, then clean the history. Tell
whoever owns the service.

Anything in a repository secret is readable by every workflow in that repo and by anyone with write
access. Scope tokens to the minimum they need.

## Dependencies

Keep lockfiles consistent with the manifest and commit both. Do not regenerate a lockfile as a side
effect of an unrelated change.

## Review

Be direct about correctness and specific about what to change. Approve when the change is right, not
when it is merely finished. If you disagree with review feedback, say why. Verify the claim before
you implement a suggestion.

## Questions

[info@advizr.ca](mailto:info@advizr.ca)
