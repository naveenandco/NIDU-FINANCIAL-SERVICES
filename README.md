# NIDU Financial Services Website

Independent website for NIDU Financial Services. Static HTML hosted on Cloudflare Pages.

## Local preview
Open `index.html` in a browser.

## Deployment
Cloudflare Pages production branch: `main`; root directory `/`; output directory `.`; no build command for the static HTML site.

## Insurance calculator notes
Health cover estimates are planning examples only. Life cover estimate uses income replacement plus liabilities and future goals, less existing cover and designated assets. Motor insurance premiums are not shown without verified insurer pricing; the calculator explains quotation factors and captures no insurer quote.

## Security limitations
Enquiry forms on the original static site prepare WhatsApp messages and store leads only in the current browser. This is not secure shared storage and must not be used as a production customer database. Configure a protected backend before collecting sensitive customer information.
