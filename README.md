# NIDU Financial Services — Fintech Portal

A static-first multi-page financial services website for NIDU Financial Services, Bengaluru.

## Public website routes

- `/` Home
- `/loans`, `/loans/business-loan`, `/loans/personal-loan`, `/loans/housing-loan`, `/loans/project-loan`, `/loans/mortgage-loan`
- `/insurance`, `/insurance/health-insurance`, `/insurance/life-insurance`, `/insurance/motor-insurance`
- `/investments`, `/investments/mutual-funds`, `/investments/sip-planner`
- `/calculators`
- `/portal` (security notice / portal placeholder)
- `/about`, `/contact`
- `/privacy-policy`, `/terms-and-conditions`, `/disclaimer`

## Business details

- Address: 20/22, 11th Main Rd, Lakkasandra Extension, Wilson Garden, Bengaluru, Karnataka 560030
- Phone: +91 98867 01942
- Support email: support@nidufinancialservices.com
- Domain: https://nidufinancialservices.com

## Features in this static release

- Responsive landing page and service routes
- Loan EMI visualizer (₹50,000–₹5 crore, 7%–24%, 1–30 years)
- Month-wise amortization download as CSV
- SIP wealth projection with inflation-adjusted estimate
- Health / life / motor insurance planning tools from the existing page
- WhatsApp contact link and Google Maps embed
- Local-business / financial-service structured data
- Legal pages with market-risk and facilitator disclosures

## Production integrations still required

This repository is a static Cloudflare Pages site. The following cannot be safely implemented with browser-only code and are not represented as live features:

1. Phone OTP — integrate an SMS provider server-side with rate limits, expiry, replay protection and abuse controls.
2. Client authentication and application status — create an authenticated API with per-customer authorization and audit logs.
3. Document upload vault — use private object storage, short-lived signed upload/download URLs, server-side validation and malware scanning; set retention/deletion rules. Never put Aadhaar, PAN, bank statements or payslips in browser local storage or public static assets.
4. CRM/Google Sheets/Zoho/HubSpot webhook — store secrets only as Cloudflare Pages/Workers secrets and validate requests server-side. Do not call a CRM API with a secret from browser JavaScript.
5. Verified reviews and partner logos — add only assets and review text for which NIDU has authorization and reliable source records. No fabricated affiliations, ratings or testimonials are included.
6. Investment distribution — publish AMFI registration / ARN and required disclosures only after the relevant status is verified. The disclaimer does not claim registration.

## Legal and regulatory notes

- Mutual fund investments are subject to market risks. Read all scheme-related documents carefully before investing.
- The site is informational; calculators are illustrative and do not promise loan approval, insurance underwriting, investment returns or premium quotes.
- Facilitator/channel-partner status is stated only where the relevant provider arrangement and authorization actually exist. Update the disclaimer to describe the exact legal relationship before publishing if this differs.
- Have the privacy notice and all regulated-product wording reviewed before enabling lead/document collection.

## Cloudflare Pages deployment

Cloudflare Pages project: `nidu-financial-services`
GitHub repository: `naveenandco/NIDU-FINANCIAL-SERVICES`
Production branch: `main`
Build command: none (static HTML)
Build output directory: `.`

Pushes to `main` are configured to trigger production deployment. Feature branches generate preview builds when Pages preview deployments are enabled. This release should be reviewed on its preview URL and merged only after the route / redirect / browser checks pass.

## Local preview

Open `index.html` in a browser. For local route testing, use a static server with SPA-style fallback to `index.html`; Cloudflare Pages can be configured with a `_redirects` file to route clean URLs to the static shell.
