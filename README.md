# Kafene

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
