<!-- One PR, one concern. If you cannot describe it in a sentence, split it. -->

## What changed

<!-- The change in one or two sentences. -->

## Why

<!-- The problem this solves. Link the issue if there is one: Closes #123 -->

## How this was verified

<!--
Required. "CI is green" is not verification on its own.
Say what you ran and what you saw. For a bugfix, confirm the test fails without the fix.
-->

- [ ] Ran the test suite locally
- [ ] Confirmed the new test fails without the fix
- [ ] Exercised the change in a running app or against a real endpoint
- [ ] Checked the error path, not just the happy path

## Risk

<!-- What could this break, and how would you notice? Write "None" if it is genuinely contained. -->

## Checklist

- [ ] Branched from the current default branch
- [ ] No secrets in the diff, the fixtures, or the commit messages
- [ ] Migrations are new and numbered, and no existing migration was edited
- [ ] Lockfile matches the manifest
- [ ] Docs updated if behavior or setup changed
