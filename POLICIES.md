# SheetFlow Finance Policies

## Information Security

* **Dependencies:** All Python dependencies are version-pinned in `requirements.txt`.
* **Vulnerability Scans:** Manual `pip-audit` run before any major deployment; high/critical issues addressed within 30 days.
* **Secrets Management:** API credentials and tokens stored in Google Cloud Secret Manager (AES-256 at rest), not in code or logs.
* **Network Security:** All communications to Cloud Functions, Plaid, and Google APIs occur over TLS 1.2+.

## Privacy Policy

* **Data Collected:** Plaid `public_token` exchanged for `access_token`; account balances and transaction history.
* **Purpose:** Import and analyze personal finance data in Google Sheets for budgeting and expense tracking.
* **Storage & Encryption:** Data resides only in the user’s Google Sheet (encrypted at rest via Google Drive).
* **Data Sharing:** No sharing with third parties; processing limited to Google Apps Script, Cloud Functions, and Plaid.
* **User Control:** Users may delete their Sheet at any time to remove data; Plaid tokens can be revoked on request.

## Data Retention & Deletion

* **Annual Process:** At the end of each calendar year, the current Sheet is retired and a new one is created for the next year.
* **User-Driven Deletion:** Users can delete their Sheet at any time to permanently remove all data.
* **Secret Revocation:** Plaid tokens and other secrets can be revoked or rotated upon request.

## Access Control

* **Google Cloud IAM:** Single owner account (Jennifer Wolfe) with Owner role; dedicated service account granted only `Secret Manager Secret Accessor` and `Cloud Functions Invoker` roles.
* **Google Sheet Sharing:** Sheets are private by default, shared only with the owner account.
* **Apps Script Properties:** Stored tokens accessible only to the script owner.

## Vulnerability Scanning

* **Scope:** Cloud Functions dependencies and local development environment.
* **Frequency:** Manual monthly `pip-audit`; results logged in GitHub Issues.
* **Remediation:** Critical findings addressed within 30 days.

## End-of-Life (EOL) Software Management

* **Inventory:** Track all Python and other dependencies with Dependabot (GitHub) or manual record.
* **Replacement Plan:** Migrate to supported versions at least 3 months before EOL.

## Multi-Factor Authentication (MFA)

* **Consumer-Facing MFA:** Institutional MFA handled by Plaid Link during account connection.
* **Internal Systems MFA:** TOTP-based MFA enabled on Google Cloud Console, GitHub, and Plaid Dashboard for all admin accounts.

## Patch Management

* **Critical Patches:** Applied within 7 days of release.
* **Regular Updates:** Dependency updates and runtime patches applied quarterly.

## Zero Trust & Centralized IAM

* **Zero Trust Principles:** Verify identity for every request; no implicit trust; use short-lived tokens.
* **Centralized Identity:** Single Google identity for ownership; service accounts for automated processes; no shared personal credentials.

---

*Last Updated: May 4, 2025*