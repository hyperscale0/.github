# Security policy

This policy covers every repository in the `hyperscale0` organization that does
not publish its own.

## Reporting a vulnerability

Report privately through GitHub private vulnerability reporting on the affected
repository. Open the repository, go to the **Security** tab, and click **Report
a vulnerability**. The report is visible to the maintainers and to you, and
nobody else.

Do not open a public issue, a pull request, or a discussion for a suspected
vulnerability. A public report is a disclosure, and it puts every user of the
package at risk before there is a fix to upgrade to.

Include what you have: the affected package and version, what an attacker can
do, and the smallest reproduction you can manage. A report without a
reproduction is still worth sending.

## What to expect

We triage the report, tell you whether we can reproduce it, and agree a
disclosure timeline with you. If we ship a fix, we credit you on the GitHub
security advisory unless you ask us not to.

We are a small team. If you have heard nothing and the wait is making you
uncomfortable, post a comment on your own private report asking for a status.

## Supported versions

Every published package is on the `1.0.0-alpha.N` line and `latest` tracks
the newest alpha. Only the most recent alpha of each package gets fixes. There
is no long-term support branch before 1.0.0, and an alpha version can change
behavior between releases.

| Package | Supported |
| --- | --- |
| `@hyperscale0/udl` | latest `1.0.0-alpha.N` |
| `@hyperscale0/hsx` | latest `1.0.0-alpha.N` |
| `@hyperscale0/adl` | latest `1.0.0-alpha.N` |
| `@hyperscale0/cli` | latest `1.0.0-alpha.N` |
| `@hyperscale0/create` | latest `1.0.0-alpha.N` |

## Scope

These repositories are libraries and tools: a format, a language front end,
an adapter vocabulary, a CLI, and a scaffolder. The libraries parse and check
untrusted input, so parser crashes,
unbounded resource use on hostile input, and validation that accepts a document
it should reject are all in scope. The Hyperscale platform itself is not in
these repositories; if you have found something in the hosted product, report
it on this repository and we will route it.
