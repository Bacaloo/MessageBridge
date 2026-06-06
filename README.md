# MessageBridge

MessageBridge is a neutral integration bridge for business messaging platforms.

The project name is intentionally platform-neutral. It must not imply that this
project is owned, endorsed, sponsored, certified, or operated by any messaging
platform provider.

## License

MessageBridge is licensed under the GNU Affero General Public License v3.0.
See [LICENSE](LICENSE).

The license applies to this project's own source code. It does not grant any
rights to third-party names, trademarks, logos, service marks, APIs, platform
accounts, message templates, or hosted services.

## Trademark And Brand Rules

This project is independent and unofficial.

Do not use third-party brand names in the repository name, package name,
application icon, logo, domain name, or other primary project identifiers.
Third-party names may be used only where necessary to accurately describe
compatibility or configuration.

Do not include third-party logos or brand assets in this repository unless a
separate written permission or a clearly applicable brand-resource license
allows that exact use.

See [TRADEMARKS.md](TRADEMARKS.md).

## Product Scope

The goal is to support the available functions of connected business messaging
platforms through provider adapters, including:

- inbound message webhooks
- outbound replies inside provider-defined service windows
- provider-approved business-initiated messages where allowed
- template or structured-message workflows where required by the provider
- media upload, download, and attachment handling
- message status and delivery webhooks
- contact and conversation metadata where made available by the provider
- audit logs and traceable message records

The bridge must not add artificial product limitations that are not required by
law, configuration, security, or the connected platform's terms. At the same
time, it must enforce provider rules where they are mandatory. For example,
some platforms require approved templates for business-initiated messages
outside a customer-service window.

## Development Principles

- Keep provider adapters separate from the neutral core.
- Keep credentials and tokens out of source control.
- Prefer official APIs and documented webhooks.
- Store enough metadata to trace inbound and outbound message processing.
- Treat opt-in, opt-out, privacy, retention, and auditability as first-class
  requirements.
- Keep public wording neutral: "supports", "integrates with", or "adapter for"
  is acceptable; "official", "certified", "by", or "endorsed by" is not unless
  there is written authorization.

