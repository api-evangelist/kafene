# Kafene

Kafene is a New York-based point-of-sale financing platform that lets retailers offer
transparent lease-to-own (LTO) purchase options to prime and non-prime consumers.
Founded in 2019 by Neal Desai and James Schuler, it underwrites shoppers with an
AI-driven risk model drawing on 20,000+ data points, returning approvals up to $5,000
in seconds, then pays the merchant directly on delivery confirmation while the customer
pays weekly or biweekly until ownership.

- Website: https://www.kafene.com
- Merchants: https://www.kafene.com/merchants
- Become a partner: https://www.kafene.com/become-a-kafene-partner
- Merchant portal: https://merchant.kafene.com/login
- Customer dashboard: https://application.kafene.com/

## API surface

As of the 2026-08-01 enrichment pass, **Kafene publishes no public API**:

- No developer portal, API reference, or documentation site
  (`developer.kafene.com` and `docs.kafene.com` do not resolve).
- No OpenAPI/Swagger, GraphQL, AsyncAPI or MCP contract found on any host.
- `api.kafene.com` resolves to Cloudflare but has **no live origin** — every path
  returns HTTP 530 / `error code: 1016`.
- No `/.well-known/` discovery documents; the 200s returned by the merchant and
  application single-page apps are HTML catch-alls, not real documents.
- No first-party SDKs in npm, PyPI, RubyGems or Packagist; no GitHub organization.

Merchant integration is arranged directly with Kafene's partner team (in-store POS
origination and text-to-apply), and Kafene is also distributed through
financing-waterfall networks such as Versatile Credit and LendPro.

See `well-known/kafene-well-known.yml` for the recorded probe matrix and
`security/kafene-domain-security.yml` for the probed TLS/DNS posture.
