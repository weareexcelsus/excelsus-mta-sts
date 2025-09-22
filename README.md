# Excelsus MTA-STS & TLS-RPT

This repository hosts the MTA-STS policy and related configuration files for the `excelsus.me` mail infrastructure.  
It ensures secure email transport by enforcing TLS encryption and providing visibility through TLS Reporting (TLS-RPT).

---

## MTA-STS Policy

- **Policy file:** `.well-known/mta-sts.txt`  
- **Version:** STSv1  
- **Mode:** enforce  
- **MX Hosts:** `mail.excelsus.me`  
- **Max Age:** 86400 seconds (24 hours)

This policy instructs external mail servers to always use STARTTLS with valid certificates when delivering mail to `excelsus.me`.

---

## TLS-RPT

TLS reporting provides daily aggregated reports from mail providers.  
These reports are sent to: tlsrpt@excelsus.me

They include details about:
- Successful TLS connections  
- Failures and downgrade attempts  
- Certificate validation issues  
