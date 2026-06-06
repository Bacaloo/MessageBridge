# MessageBridge Programming Rules

These rules are binding for all future code changes in this repository.

## Repository Purpose

- MessageBridge is a neutral business messaging integration bridge.
- The repository name, package names, namespaces, app identifiers, icons, and
  UI branding must stay neutral.
- Provider names may be used only in descriptive documentation, configuration
  labels, or provider adapter names where technically necessary.

## Licensing

- All project code is licensed under GNU AGPLv3 unless a file explicitly states
  a compatible license.
- Do not copy code from another project unless its license is compatible with
  AGPLv3 and the origin is documented.
- Do not add dependencies with unclear, proprietary, non-commercial, source
  available, SSPL, BUSL, or advertising-style license terms without prior
  review.
- The repository license does not grant rights to third-party trademarks,
  logos, service names, APIs, hosted services, or message templates.

## Trademark And Provider Rules

- Do not include third-party logos or brand assets.
- Do not imply partnership, sponsorship, certification, or endorsement by any
  provider.
- Do not use provider names in primary project identifiers.
- Any provider-specific behavior must be isolated in a provider adapter.
- Provider policy restrictions must be documented before or with the code that
  enforces them.

## WhatsApp-Specific Boundary

- Do not implement WhatsApp Web, browser automation, QR-session automation,
  unofficial reverse-engineered clients, or scraping-based access.
- Use only official, documented APIs for provider adapters intended for
  production use.
- Business-initiated messaging must be supported only through provider-approved
  mechanisms where the provider requires them, such as approved templates.
- The bridge must not add artificial product limitations that are not required
  by law, security, configuration, or provider policy.

## Data Protection

- Never commit access tokens, refresh tokens, webhook secrets, app secrets,
  phone numbers, customer payloads, production message bodies, production media,
  or identifiable contact data.
- Examples must use synthetic data only.
- Webhook payloads used in tests must be synthetic and minimal.
- Auditability is mandatory: inbound events, outbound attempts, and provider
  status callbacks must be traceable.

## Architecture

- Keep the neutral core free of provider-specific assumptions.
- Keep provider adapters behind stable interfaces.
- Keep storage concerns behind a repository/store interface.
- Keep Nextcloud integration behind an adapter boundary.
- Prefer small, explicit modules over cross-cutting helper magic.
- Avoid vendor lock-in in core data structures.

## Quality

- Add or update tests for behavior changes.
- Keep code deterministic and side-effect-light where practical.
- Validate inbound HTTP payloads before processing.
- Do not silently drop provider errors; record them as status or audit events.
- Preserve message state transitions carefully.

