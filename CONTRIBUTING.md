# Contributing

This applies to every repository in the `hyperscale0` organization that does not
publish its own guide.

## Before you write code

Open an issue first for anything larger than a typo or an obvious bug fix. The
open repositories are a document format, a language front end, and an adapter
vocabulary, so a change to any of them is a change to a contract other people
have already written files against. Agreeing the shape in an issue is cheaper
than rewriting a pull request.

The append-only rule governs the format and the language: adding a new optional
field, a new state, or a new verb is fine, and removing one, renaming one, or
tightening an existing validation breaks documents that already exist. Expect a
change in the second category to be refused or deferred to the next format
version.

## Contributor License Agreement

Contributions are accepted under a CLA. A bot comments on your first pull
request with the agreement and records your acceptance. We do not use DCO
sign-off, so `git commit -s` is not required and does not substitute.

We ask for a CLA because Hyperscale owns these languages and needs to keep the
freedom to relicense them. Your contribution stays yours; the CLA grants us the
rights to ship it.

## Commits

Conventional Commits: `type(scope): summary` in the imperative, lower case, no
trailing period.

```
feat(parser): accept scoped ids in aggregate references
fix(validation): reject a lifecycle with no terminal state
docs(readme): correct the canonical serializer example
```

Types in use: `feat`, `fix`, `docs`, `test`, `refactor`, `chore`, `perf`. Keep
one logical change per commit. The commit message says what the change does and
why, and skips the essay.

## Tests are required

A pull request that changes behavior includes tests. A bug fix includes a test
that fails without the fix. New parsing or validation behavior includes a
fixture, because the fixture suites are the executable specification for these
projects and prose about the grammar drifts from the grammar.

Run the repository's own check task before you push. Each repository documents
it in its README, and CI runs the same thing on your pull request.

## Pull requests

Keep the diff to one concern. Say what changed and how you verified it; the
pull request template asks for exactly that. A pull request that reformats
unrelated files is hard to review and will be sent back.

Public repositories build on GitHub-hosted runners. CI has to be green before
review is worth anyone's time.
