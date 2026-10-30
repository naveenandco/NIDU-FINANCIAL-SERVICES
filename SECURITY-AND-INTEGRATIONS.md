# Production integration checklist

This release deliberately does not collect sensitive identity or financial documents.

Before enabling the client portal:
- Create Cloudflare Worker/Pages Functions API endpoints.
- Store customer records in a protected database (for example D1) with customer-scoped authorization and audit logs.
- Use an OTP vendor only from server-side code; hash OTP challenge state, expire quickly, rate-limit sends and attempts, and protect against enumeration.
- Use private R2 buckets for documents. Issue short-lived signed uploads only after authentication; validate MIME signatures, file size and malware scan results server-side.
- Never store OTPs, Aadhaar/PAN, bank statements, salary slips, access tokens or CRM credentials in localStorage or static JavaScript.
- Define data minimization, retention, deletion, grievance and breach-response procedures before accepting uploads.
- Add CSRF/origin checks, bot protection, abuse throttles, input validation and security headers.
- Integrate CRM webhooks from a server-side function. Keep webhook URLs and API keys in Cloudflare secrets.
- Perform a security review and privacy/legal review before making the portal publicly available.

Calculators are illustrative only. Do not treat them as loan sanction or lender eligibility. Investment illustrations do not guarantee market returns. Obtain compliance review for product claims and distribution disclaimers.
