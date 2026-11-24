# Evidence log — CTI-001

| ID | Source | Recorded result | Limitation |
|---|---|---|---|
| E01 | Original SMS | UPS customs-charge pretext; non-brand domain | Sender redacted; spoofing possible |
| E02 | DNS A / PTR | IP and reverse name | Time-specific |
| E03 | [RIPE Database](https://apps.db.ripe.net/db-web-ui/query) | Route and origin ASN | No attacker attribution |
| E04 | [Malwarebytes](https://www.malwarebytes.com/) | Suspicious verdict; registration and registrar | Vendor-reported |
| E05 | [crt.sh](https://crt.sh/) | Empty arrays | Coverage limitations |
| E06 | [HackerTarget](https://hackertarget.com/reverse-ip-lookup/) | No DNS A records | Coverage limitations |
| E07 | [URLScan](https://urlscan.io/) | Zero results; 30-day window | Coverage limitations |
| E08 | SMTP rejection | 554 5.7.1 rspamd filter | Does not establish intent |

Public log summarizes investigator-reported evidence, not raw captures. No hashes or precise collection timestamps are claimed where unavailable.
