# Business & jurisdiction configuration

Values that only the business owner can supply. **None of these may be invented.**
Unfilled values are launch blockers where marked.

| Key | Value | Launch blocker? |
|---|---|---|
| BUSINESS_LEGAL_NAME | `[LEGAL ENTITY NAME REQUIRED]` | Yes |
| BUSINESS_ENTITY_TYPE | `[ENTITY TYPE REQUIRED]` | Yes |
| BUSINESS_COUNTRY | `[BUSINESS COUNTRY REQUIRED]` | Yes |
| REGISTERED_ADDRESS | `[REGISTERED ADDRESS REQUIRED]` | Yes |
| BUSINESS_EMAIL | `[BUSINESS EMAIL REQUIRED]` | Yes |
| SUPPORT_EMAIL | `[SUPPORT EMAIL REQUIRED]` | Yes |
| PRIVACY_EMAIL | `[PRIVACY EMAIL REQUIRED]` | Yes |
| VAT_NUMBER | `[VAT NUMBER — AS APPLICABLE]` | Depends on country |
| COMPANY_REGISTRATION_NUMBER | `[REGISTRATION NUMBER — AS APPLICABLE]` | Depends on country |
| PRIMARY_TARGET_MARKET | To be set by DECISION from Strategy stage | — |
| ADDITIONAL_TARGET_MARKETS | To be set by Strategy stage | — |
| CUSTOMER_TYPE | To be set by Strategy stage | — |
| GOVERNING_LAW | `[TO BE DETERMINED — depends on BUSINESS_COUNTRY]` | Yes |
| DISPUTE_JURISDICTION | `[TO BE DETERMINED — depends on BUSINESS_COUNTRY]` | Yes |
| PAYMENT_PROVIDER | To be chosen by Architecture stage | — |
| HOSTING_PROVIDER | To be chosen by Architecture/DevOps stage | — |
| EMAIL_PROVIDER | To be chosen by Architecture stage | — |
| ANALYTICS_PROVIDER | To be chosen by Architecture stage | — |
| ERROR_MONITORING_PROVIDER | To be chosen by Architecture stage | — |

The application reads operator-supplied values (legal name, addresses, contact emails) from
environment variables at runtime so that production can be configured without editing source code.
When a value is not configured the public pages render an explicit placeholder rather than
fabricated information.
