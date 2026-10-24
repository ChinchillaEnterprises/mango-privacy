# Mango Privacy Policy

Last updated: 2026-10-24

Chrome Web Store version 0.1.0.217. Operator: Chinchilla AI.

Mango is a Chrome extension built by Chinchilla AI, with a companion application that runs on the same computer. It lets Chinchilla's own software agents operate a Chrome browser on our own machines. It is for internal use by Chinchilla agents only and is distributed as Unlisted on the Chrome Web Store. It is not offered to the public.

This policy describes only the Chrome Web Store build of the extension (version 0.1.0.217) and its companion application. It does not describe the separate self-hosted build of the extension.

## What Mango handles

When an agent uses Mango on a page, Mango can read the page (text, structure, accessibility information, URL, tab and frame information), network request and response headers for the agent's own tabs (cookie and authorization headers are redacted), and take screenshots. Fields that look like passwords, card numbers or one-time codes are masked in screenshots. If another browser extension blocks Mango's debugger access, Mango cannot mask, so it refuses to capture any page that contains such a field. Masking is heuristic and is not a guarantee that every secret on a page is detected. Typed text and form values are not written to Mango's action log.

## Credential filling

When an agent asks Mango to fill a login or card field from a password vault, the companion application (not the extension) retrieves the value, and only if that vault and item are permitted for that agent under the companion's configured access rules. Anything not permitted is refused. The companion passes the value to the extension, which enters it into the requested field. The extension does not access the password vault itself. The value is not returned to the agent, except that for a card-number field the last four digits are returned. Fields filled this way are masked in later screenshots.

## Where it goes

- The extension makes no web requests of its own. It talks only to the companion application on the same computer.
- The companion returns page content and screenshots to the Chinchilla agent that asked for them. That agent runs on the same machine or, if enabled for that machine, on our private network.
- Page content and screenshots are sent to our AI model providers (Anthropic and OpenAI) to do the task.
- What an agent or its AI model provider does with that content afterwards is governed by the provider's own terms and is not otherwise established by this policy.
- Mango has no analytics or advertising code.

## What we do not do

- This data is never sold or shared for advertising.
- Chinchilla does not train on it; providers process it under their own terms.

## No remote code

The extension runs only code packaged with it. It does not download or execute remotely supplied code. The tool that evaluated JavaScript supplied by an agent is disabled in this build and returns an error. Agent commands select built-in operations and supply data (for example coordinates or text); those built-in operations run fixed, packaged scripts in the browser page.

## How long we keep it

- Browser session state (including a log of up to 1,000 recent actions with typed values excluded) is cleared when the browser quits or the extension reloads.
- When another screenshot file is saved for a tenant, the companion attempts to remove files in that tenant's capture directory that are more than 24 hours old. Files may remain longer if no further captures occur or cleanup fails. This does not delete recipient copies.
- The companion's diagnostic logs have no automatic retention limit and may persist until deleted by hand.
- Copies held by agents or their providers are not covered by these periods.
- Removing the extension does not delete files the companion application has saved (such as screenshot files and diagnostic logs) or copies held by agents or their providers.

## Contact

Chinchilla AI: administration@chinchilla-ai.com
