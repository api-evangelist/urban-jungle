# Urban Jungle (urban-jungle)

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
