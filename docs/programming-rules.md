# Programming Rules

MessageBridge is intended to be publishable. Treat every change as if it may
later become public.

## Core Rules

1. Keep the project name and primary identifiers provider-neutral.
2. Keep provider-specific logic in provider adapters.
3. Use official, documented provider APIs for production adapters.
4. Do not implement unofficial WhatsApp Web automation or reverse-engineered
   clients.
5. Keep credentials and production data out of Git.
6. Document platform restrictions that shape behavior.
7. Test message state transitions and provider error handling.
8. Preserve AGPLv3 compatibility for copied code and dependencies.

## Messaging Rules

- Incoming messages are stored as provider events and normalized messages.
- Outgoing messages are created as send requests and move through explicit
  states.
- Status callbacks update existing messages or send attempts; they must not be
  treated as unrelated new conversations.
- Provider IDs are stored as external references, not as internal primary keys.
- Business-initiated messages are allowed only when the provider adapter can
  prove the requested send mode is permitted by configuration and provider
  policy.

## Documentation Rules

- Provider names may be used descriptively.
- Brand names must not be used in repository names, package names, domains,
  icons, or primary UI branding.
- Public documentation must include the independent-project disclaimer when it
  mentions a provider.

