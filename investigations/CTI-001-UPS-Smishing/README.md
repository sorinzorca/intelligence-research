# CTI-001 — Suspected UPS smishing in Romania

**Observed:** 24 November 2026, approximately 11:32 EET.
**Assessment:** Suspected smishing and brand impersonation. High confidence in the suspicion; malicious landing-page behavior remains unverified.

An unsolicited SMS claiming customs charges were due directed the recipient to a non-UPS domain. The displayed sender number is withheld; spoofing cannot be excluded.

## Technical observations

| Indicator | Value | Provenance |
|---|---|---|
| Domain | livrari-premium[.]com | SMS |
| IPv4 | 45.141.215.167 | Investigator DNS A lookup |
| PTR | 45.141.215.167.powered.by.rdp.sh. | Investigator reverse DNS lookup |
| Route | 45.141.215.0/24 | RIPE WHOIS |
| Origin | AS210558 | RIPE WHOIS |
| Registrar | Tucows | Malwarebytes domain lookup |
| Registration | 2026-11-23 17:01:36 UTC | Malwarebytes domain lookup |
| Reputation | Suspicious | Malwarebytes URL lookup |

The reported registration timestamp preceded SMS receipt by approximately 16 hours 30 minutes. This is a risk signal, not proof of fraud.

## Passive investigation

Certificate transparency searches returned empty arrays. HackerTarget reverse IP returned no DNS A records. URLScan domain and IP searches returned zero results within the reported 30-day window. These results do not establish absence of certificates, other hosted domains or malicious activity.

## Abuse reporting

An email to the RIPE-listed abuse contact was attempted and rejected with SMTP 554 5.7.1 (rspamd filter). Successful delivery and takedown are not established.

## Limitations

No direct landing-page visit was documented. Credential collection, payment mechanisms, operator identity, victim count and attribution remain unverified. Infrastructure providers are not presumed complicit. Raw evidence is not publicly reproduced; results are investigator-reported and time-specific.

## Reference services

- [RIPE Database](https://apps.db.ripe.net/db-web-ui/query)
- [Certificate Transparency](https://crt.sh/)
- [URLScan](https://urlscan.io/)
- [HackerTarget](https://hackertarget.com/reverse-ip-lookup/)
- [Malwarebytes](https://www.malwarebytes.com/)

## Defensive recommendations

Do not visit the suspicious domain. Verify delivery charges through official carrier channels independently of the SMS. Preserve suspicious messages and report them through official abuse channels.
