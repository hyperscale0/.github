# Hyperscale

Hyperscale is financial infrastructure for Saudi Arabia. A tenant describes a
financial product in HSX, a small language. The platform compiles that
description and runs the money movement against partner banks through a bank
reference model. Hyperscale is never itself a fintech and never a TPP. We host
the control plane, meaning the engine, the portal, and the registry, and none
of the tenant's runtime.

## What is open

The language and the format layer are open source under Apache-2.0.

| Repo | What it is | License | npm |
| --- | --- | --- | --- |
| [udl](https://github.com/hyperscale0/udl) | The document format. Parser, validator, and canonical serializer for `.udl` documents. | Apache-2.0 | `@hyperscale0/udl` |
| [hsx](https://github.com/hyperscale0/hsx) | The language. Lexer, parser, checker, and compiler down to an IR. | Apache-2.0 | `@hyperscale0/hsx` |
| [provider-adapter](https://github.com/hyperscale0/provider-adapter) | The adapter format, its conformance suite, and the authoring guide. | Apache-2.0 | `@hyperscale0/provider-adapter` |
| [starters](https://github.com/hyperscale0/starters) | Starter applications. Coming. | MIT | none |

## What is not open

The runtime that executes the IR is proprietary. The split is the one HashiCorp
drew between HCL and Terraform: you can read, parse, check, and compile the
language without us, and the thing that runs the result is the product we sell.
Anything you write in HSX or `.udl` stays yours, and the tools that read it are
Apache-2.0, so nothing you author is locked to a runtime you cannot inspect.

## Install the libraries

There is no scaffolding command yet. Install the packages directly.

```bash
npm install @hyperscale0/udl@alpha
npm install @hyperscale0/hsx@alpha
npm install @hyperscale0/provider-adapter@alpha
```

Every package is `1.0.0-alpha.N` and publishes to the `alpha` dist-tag. The
`latest` tag stays unset until 1.0.0, so an install without `@alpha` fails
instead of quietly resolving to something we have not stabilized yet.

## Contributing

Read [CONTRIBUTING.md](https://github.com/hyperscale0/.github/blob/main/CONTRIBUTING.md)
before opening a pull request. It covers the CLA, commit style, and the test
bar. Issues and pull requests belong on the specific repo, not here.

Discussion of the format and the language happens in the open. If a seam our
own adapters need is missing from `provider-adapter`, that is a bug in the kit,
because first-party adapters use exactly the published kit and nothing more.

## Security

Report vulnerabilities through GitHub private vulnerability reporting on the
affected repo, under its Security tab. Do not open a public issue for a
vulnerability. Full policy:
[SECURITY.md](https://github.com/hyperscale0/.github/blob/main/SECURITY.md).

## Trademarks

The name "Hyperscale" and the Hyperscale logo are not licensed under
Apache-2.0. The code license covers the code. It does not grant permission to
use the marks for your own product, service, or organization.

[hyperscale0.ai](https://hyperscale0.ai)
