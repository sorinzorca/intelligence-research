# CTI-001 — Suspected UPS smishing in Romania

Status: editorial revision approved for publication.
Editorial review date: 24 November 2026.
Source baseline: sorinzorca/intelligence-research, main tree be855609728ee20110fb9012c1d3addf49cf966f.
Repository path: investigations/CTI-001-UPS-Smishing/technical-report.md.

## Scope and provenance

This revision consolidates the existing public README, technical report, timeline, indicators and evidence log. Those documents report an unsolicited UPS-themed customs-charge SMS received in Romania at approximately 11:32 EET (09:32 UTC) on 24 November 2026. Original SMS and raw lookup captures were unavailable to this review. No independent DNS, registry, certificate, reputation or landing-page examination was performed here. Verified access to the repository does not validate its underlying evidence.

## Reported observations

| Item | Existing record | Qualification |
|---|---|---|
| SMS pretext | UPS customs charges; destination livrari-premium[.]com | Investigator-reported; original image unavailable |
| DNS A | 45[.]141[.]215[.]167 | Historical reported association; collection time unavailable |
| PTR | 45[.]141[.]215[.]167[.]powered[.]by[.]rdp[.]sh | Association only; not operator identity |
| Route / origin | 45[.]141[.]215[.]0/24; AS210558 | Reported RIPE WHOIS result; not a blocking recommendation |
| Registrar / registration | Tucows; 2026-11-23 17:01:36 UTC | Reported Malwarebytes result, not a new registry verification |
| Reputation | Suspicious | Vendor-reported label at the earlier lookup time |
| CT searches | Empty arrays for domain and subdomains | Query details and raw responses unavailable |
| Reverse IP | No DNS A records from HackerTarget | Coverage-limited result |
| URLScan | Zero domain/IP results in reported 30-day window | Search time and exact queries unavailable |
| Abuse report | SMTP 554 5.7.1, rspamd filter | Rejection reported; delivery and takedown unverified |
| UPS support acknowledgment | Investigator supplied email text acknowledging a support request and assigning a case number | Original email and headers not inspected; authenticity and timestamp unverified; case number withheld |

## Timeline and calculation

Reported registration: 23 November, 17:01:36 UTC. Reported receipt: approximately 24 November, 09:32 UTC. Subtraction yields approximately 16h 30m (16h 30m 24s if the rounded receipt time is treated as exact). Receipt precision does not support a seconds-precise interval. Lookup and abuse-email times are not reconstructed.

## Assessment

### Support-report update

During this review the investigator supplied the text of an email attributed to UPS Customer Service, with the subject referring to suspected UPS impersonation via SMS in Romania. The text states that the request was received, assigns a case number and says Customer Service will respond. This is distinct from the earlier rejected email to the network abuse contact. It records a reported acknowledgment only: no substantive UPS verdict, domain investigation, delivery to the network abuse contact or takedown is established. No exact acknowledgment time is inferred. Original headers and authentication results were not available; authenticity has not been independently verified. The case identifier is omitted from publication materials.

### Threat assessment

The reported branding/payment pretext, non-brand destination, recent registration and reputation label are consistent with suspected smishing. Confidence in the original observation set is bounded by unavailable primary evidence; this review does not independently upgrade it. Landing-page behavior and malicious functionality remain unverified.

No attacker identity, geographic origin, victim count, credential capture, payment mechanism or financial loss is established. A displayed phone number would not by itself establish the originating subscriber. Network, registrar and hosting associations do not establish wrongdoing or complicity.

## Privacy and publication controls

Sender and recipient numbers are omitted in full. No raw image, tracking number, message identifier, personal query token or phone metadata is included. There is no screenshot in this release candidate to redact. If an image is added later, create a flattened redacted derivative, remove metadata, inspect it visually and check OCR before approval; preserve the original privately. Do not publish original-image hashes as though originals were inspected in this review.

All suspect domain/IP renderings above are defanged. Route and ASN are contextual, not a blanket blocklist. No sample was uploaded to a public scanner and no suspect URL was visited during this review.

## Evidence gaps and next checks

Obtain the original SMS privately and inspect a redacted derivative; record provenance, collection time and timezone. Obtain original lookup outputs and exact search scopes where available. Any new passive checks must be logged as new observations with their own timestamp, without rewriting historical values. Do not infer the original site’s behavior from a later result. Record corrections in a dated change log.

## Sources

- [Existing case overview](https://github.com/sorinzorca/intelligence-research/blob/main/investigations/CTI-001-UPS-Smishing/README.md)
- [Existing evidence log](https://github.com/sorinzorca/intelligence-research/blob/main/investigations/CTI-001-UPS-Smishing/evidence-log.md)
- [Existing timeline](https://github.com/sorinzorca/intelligence-research/blob/main/investigations/CTI-001-UPS-Smishing/timeline.md)
- [UPS fraud guidance](https://www.ups.com/us/en/support/shipping-support/legal-terms-conditions/fight-fraud), checked 24 November 2026; general defensive context only, not confirmation of this case.
