# Lightspeed Photonics

LightSpeed Photonics is a silicon-photonics and optoelectronics hardware company building optical
interconnect for computing — "Bringing Light to the Computing World." Its public site covers the
LightKonnect product line (LightKonnect and LightKonnect Fiber), LightSIP technology, patents and
publications, and an Insights area with blog, news and events.

Backed by: 500-global — https://lightspeedphotonics.com

## Enrichment status

Enrichment pass 2026-07-19: **no API surface**. LightSpeed Photonics is a semiconductor and optical
hardware vendor, not an API provider. It publishes no public API, developer portal, documentation,
SDK, or machine-readable specification.

Verified during the pass:

- No GitHub organization (three name variants all 404).
- No `docs.` / `api.` / `developer.` / `status.` / `trust.` subdomains resolve.
- The site is a React SPA with a **catch-all rewrite**: every unknown path returns HTTP 200 with the
  `index.html` shell. `/.well-known/*`, `/llms.txt`, `/robots.txt` and `/openapi.json` are therefore
  **soft 404s** — see `well-known/lightspeed-photonics-well-known.yml`, which body-verifies each one.
  Do not read those 200s as published documents.
- No vulnerability disclosure program and no trust center.

Artifacts present: `security/` (probed TLS/DNS posture) and `well-known/` (negative-result index).
