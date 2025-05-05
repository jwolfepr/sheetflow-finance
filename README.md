# sheetflow-finance
Google Sheets dashboard for personal finance powered by Plaid

# SheetFlow Finance

SheetFlow Finance is a personal finance dashboard built in Google Sheets, leveraging Plaid for secure account connectivity and data aggregation.

This repository contains:

* **`POLICIES.md`**: Streamlined policy documentation.
* A **Compliance Dashboard** below to track completion of security and governance tasks.

---

## Policies

* [POLICIES.md]

---

## Compliance Dashboard

### One-Time Tasks (Baseline)

| Task                                             | Due Date   | Status | Link           |
| ------------------------------------------------ | ---------- | :----: | :------------- |
| Publish `POLICIES.md` to GitHub                  | 2025-05-15 |    ✔   | [POLICIES.md](https://github.com/jwolfepr/sheetflow-finance/blob/main/POLICIES.md) |
| Adopt EOL Management (Dependabot)                | 2025-05-31 |    ☐   | \[create link] |
| Enable Vulnerability Scans                       | 2025-05-31 |    ☐   | \[create link] |
| Publish Privacy Policy (Google Doc → GitHub)     | 2025-05-10 |    ☐   | \[create link] |
| Implement Access Control (IAM review & lockdown) | 2025-05-20 |    ☐   | \[create link] |
| Enable Consumer MFA (Plaid Link)                 | 2025-05-15 |    ☐   | \[create link] |
| Enable Internal MFA (Google, GitHub, Plaid)      | 2025-05-15 |    ☐   | \[create link] |
| Document Zero Trust Approach                     | 2025-06-01 |    ☐   | \[create link] |
| Secure Tokens & Certificates                     | 2025-05-25 |    ☐   | \[create link] |
| Define Patch Management SLA                      | 2025-06-01 |    ☐   | \[create link] |

### Recurring Tasks (Operational)

| Cadence   | Task                                             | First Due  | Status       | Link           |
| --------- | ------------------------------------------------ | ---------- | ------------ | :------------- |
| Monthly   | Run `pip-audit` & address critical findings      | 2025-06-30 | 🔁 monthly   | \[create link] |
| Monthly   | Review Cloud Logging & uptime checks             | 2025-06-30 | 🔁 monthly   | \[create link] |
| Quarterly | Conduct IAM access review                        | 2025-07-15 | 🔁 quarterly | \[create link] |
| Quarterly | OWASP ZAP quick scan of front-end launcher       | 2025-07-15 | 🔁 quarterly | \[create link] |
| Annual    | Full policy review & update (`POLICIES.md`)      | 2025-11-04 | 🔁 annual    | \[create link] |
| Annual    | Test incident response playbook & rotate secrets | 2025-11-04 | 🔁 annual    | \[create link] |
| Annual    | Manual Year-End Sheet Retirement                 | 2025-12-31 | 🔁 annual    | \[create link] |

---

*Last updated: May 4, 2025*
