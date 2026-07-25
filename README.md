# Urban Jungle (urban-jungle)

Urban Jungle Services Ltd is a London-based direct-to-consumer insurtech, founded in 2016 by Jimmy Williams and Greg Smyth to sell home insurance to "Generation Rent" — renters, sharers and students the traditional UK market underserves. It is an FCA-authorised intermediary (FRN 782061, company number 10414152, England and Wales) and a certified B Corp, selling contents, buildings and contents, students contents, tenants liability, landlord, home emergency and public liability cover through its own digital journey at myurbanjungle.com, and claiming over 100,000 customers. Its API posture is partner-gated and undocumented in public.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/urban-jungle/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/urban-jungle/refs/heads/main/apis.yml)

## Tags

- Insurance
- United Kingdom
- Insurtech
- Property and Casualty
- Home Insurance
- Renters Insurance
- Embedded Insurance
- Underwriting
- Broker
- Direct to Consumer

## Timestamps

- **Created:** 2026-07-25
- **Modified:** 2026-07-25

## APIs

None listed. Urban Jungle publishes no public, self-serve API.

The company announced a partnership programme and quote API in 2018 so that lettings agents, PropTech firms, institutional landlords and eCommerce sites could serve Urban Jungle quotes inside their own products without being directly FCA-regulated. That API is real, but it is entirely partner-gated. There is no developer portal, no reference documentation, no OpenAPI or Swagger definition, no published authentication scheme, no webhook or event catalog, no public Postman collection, no GraphQL endpoint and no company GitHub organization. The only documented route to integration is `partnerships@myurbanjungle.com`.

The partner page offers three integration models:

- **Simple Referral** — a partner account and a unique referral link.
- **API Integration** — "Give customers a personalised quote, on your site or app," with unpublished sample code.
- **Journey Wrap** — "Wrap our journey in your experience or send customers to our site."

Of the four insurance API verbs, only **quote** is exposed, and only to partners. **Bind**, **issue** and **FNOL** stay inside Urban Jungle's own journey; there is no claims API of any kind.

### ACORD posture

**No ACORD reference found.** A case-insensitive search for ACORD, AL3, ACORD XML and NGDS returned zero hits across the rendered site and the Angular application bundles. Expected for a UK direct-to-consumer digital intermediary with no agency-management-system distribution.

### Domain note

The assigned primary domain `urbanjungle.com` is **not** this company — it returns HTTP 202 behind a Sucuri captcha challenge and serves no Urban Jungle Insurance content. The real operating domain is **myurbanjungle.com**.

### Probe note

`myurbanjungle.com` is an Angular single-page app that soft-404s: `/developers`, `/openapi.json` and a deliberately bogus `/zzzznonexistent1234` all return HTTP 200 with a byte-identical shell. Path status codes are therefore worthless here, and the real route table was read out of `main-KZKSFKYK.js` instead. It contains no developer, docs, api or reference route. `api.myurbanjungle.com` answers 200 with a two-byte `OK` from gunicorn and 404s on every specification path — a health endpoint for the first-party web app, not a documented API.

## Links

- [Website](https://myurbanjungle.com/)
- [About](https://myurbanjungle.com/about_us)
- [Partnership Programme](https://myurbanjungle.com/partners)
- [Blog](https://myurbanjungle.com/explore/blog/)
- [Careers](https://myurbanjungle.com/explore/careers/)
- [Meet the Team](https://myurbanjungle.com/explore/meet-the-team/)

## Review

See [review.yml](review.yml) for the full reviewer finding, every probed URL with its HTTP status, and provenance.
