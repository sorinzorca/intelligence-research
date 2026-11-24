# Technical report — CTI-001

## Scope
Passive analysis of a suspicious SMS received in Romania on 24 November 2026 at approximately 11:32 EET (09:32 UTC). Sender withheld. No direct site interaction documented.

## Collection and analysis
- SMS: customs-charge pretext, UPS branding, destination livrari-premium[.]com.
- DNS A: 45.141.215.167; reverse DNS: 45.141.215.167.powered.by.rdp.sh.
- RIPE WHOIS: route 45.141.215.0/24, origin AS210558.
- Malwarebytes lookup: suspicious verdict, Tucows registrar, registration 2026-11-23 17:01:36 UTC.
- Registration-to-receipt interval: approximately 16h 30m (09:32 UTC next day minus 17:01:36 UTC).
- Certificate transparency: empty arrays for domain and subdomain searches.
- HackerTarget reverse IP: no DNS A records returned.
- URLScan: zero results for domain and IP in reported 30-day search window.

## Assessment
The brand/payment pretext, non-brand destination, recent registration and suspicious verdict support a suspected smishing assessment. DNS and registry records establish observed associations only; they do not identify an attacker. Negative search results are bounded by source coverage.

## Response
Network abuse email rejected with SMTP 554 5.7.1 (rspamd filter). No takedown or successful delivery to that contact verified.

## Limitations
No verified landing-page content, credential capture, payment mechanism, victim count or attribution. Raw evidence is withheld; public results are investigator-reported. See [evidence log](evidence-log.md).
