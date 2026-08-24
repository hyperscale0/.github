# Hyperscale

Hyperscale is financial infrastructure for Saudi Arabia. A tenant describes a
financial product in HSX, a small language. The platform compiles that
description and runs the money movement against partner banks through a bank
reference model. Hyperscale is never itself a fintech and never a TPP. We host
the control plane, meaning the engine, the portal, and the registry, and none
of the tenant's runtime.

## What is open

The language and the format layer are open source under AGPL-3.0-only, with a
commercial license available for anyone the copyleft does not fit. Each
repository's `LICENSING.md` explains the two tracks. The starters are MIT.

| Repo | What it is | License | npm |
| --- | --- | --- | --- |
| [hyperscale-udl](https://github.com/hyperscale0/hyperscale-udl) | The document format. Parser, validator, and canonical serializer for `.udl` documents. | AGPL-3.0-only | `@hyperscale0/udl` |
| [hyperscale-hsx](https://github.com/hyperscale0/hyperscale-hsx) | The language. Lexer, parser, checker, and compiler down to an IR. | AGPL-3.0-only | `@hyperscale0/hsx` |
| [hyperscale-adl](https://github.com/hyperscale0/hyperscale-adl) | The adapter format, its conformance suite, and the authoring guide. | AGPL-3.0-only | `@hyperscale0/adl` |
| [hyperscale-starters](https://github.com/hyperscale0/hyperscale-starters) | Starter applications in Go, Python, and TypeScript. | MIT | none |

## What is not open

The runtime that executes the IR is proprietary. The split is the HCL and
Terraform one: you can read, parse, check, and compile the language without us,
and the thing that runs the result is the product we sell.
Anything you write in HSX or `.udl` stays yours, and the tools that read it are
open source, so nothing you author is locked to a runtime you cannot inspect.

## Install

```bash
npm install @hyperscale0/udl
npm install @hyperscale0/hsx
npm install @hyperscale0/adl
```

Two tools ship alongside the libraries, free to use and proprietary-licensed:
`npm create @hyperscale0` scaffolds a starter app, and `npx @hyperscale0/cli`
drives a Product's operation surface with an API key.

Every package is on the `1.0.0-alpha.N` line and `latest` tracks the newest
alpha. Alpha versions can change behavior between releases.

## Contributing

Read [CONTRIBUTING.md](https://github.com/hyperscale0/.github/blob/main/CONTRIBUTING.md)
before opening a pull request. It covers the CLA, commit style, and the test
bar. Issues and pull requests belong on the specific repo, not here.

Discussion of the format and the language happens in the open. If a seam our
own adapters need is missing from the adapter kit, that is a bug in the kit,
because first-party adapters use exactly the published kit and nothing more.

## Security

Report vulnerabilities through GitHub private vulnerability reporting on the
affected repo, under its Security tab. Do not open a public issue for a
vulnerability. Full policy:
[SECURITY.md](https://github.com/hyperscale0/.github/blob/main/SECURITY.md).

## Trademarks

The name "Hyperscale" and the Hyperscale logo are not licensed with the code.
The code licenses cover the code. They do not grant permission to use the
marks for your own product, service, or organization.

[hyperscale0.ai](https://hyperscale0.ai)
