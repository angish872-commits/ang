# Globle Pets — Starter Website

A lightweight, responsive pet-project concept for **Globle Supply Chain** at `pets.globlesupplychain.com` (suggested future subdomain).

**Status:** Deployed to Cloudflare Pages at https://globle-pets-site.pages.dev . The custom domain `pets.globlesupplychain.com` has been registered and its CNAME created; Cloudflare certificate/domain validation may still be pending. No products, services, prices, launch dates, or availability have been announced.

## Three sections
1. **Welcome** — introduction and friendly pet-focused concept.
2. **Coming Soon** — possible product, care and community ideas, clearly marked as exploratory.
3. **Requests** — visitors can describe what they hope to see.

## Run locally
Open `index.html` in a browser. No build process, frameworks, tracking scripts or external assets required.

## Request handling — IMPORTANT
There is **no request-collection backend** and the app never claims otherwise.
- Set `requestEmail` in `config.js` *only after* verifying that this mailbox really exists and can receive mail. Then visitors can compose an email in their own email app.
- Until then the request page offers a **Copy request** action. Copying is not sending; users are told that explicitly.
- Request form data is not stored in a database or browser local storage. This initial version has no admin dashboard or customer database.
- Before enabling production request submissions, add server-side validation, spam prevention, privacy and data-retention policies, and a legitimate confirmed recipient or backend.

## Deployment via Cloudflare Pages
A **separate** GitHub-backed Cloudflare Pages project, `globle-pets-site`, was created. The MoveFuel project was not changed.

The steps below document the configuration already applied and how to maintain it:
1. Keep the **separate** Cloudflare Pages project for this repository. Do **not** edit or reuse `movefule-website`.
2. Set the framework preset to **None**; build command empty; output directory `/` (repository root).
3. Preview and verify all three tabs.
4. Add `pets.globlesupplychain.com` as a custom domain in that new Pages project; allow Cloudflare to create the necessary DNS record.
5. **Preserve** all existing root, `www`, MX, TXT, DKIM and other email records. This project intentionally does not touch them.
6. If your father later prefers the main domain, plan that migration separately rather than replacing the corporate root unexpectedly.

## Editing content
- `index.html` — copy and three dashboard sections
- `styles.css` — responsive design
- `app.js` — navigation and request preparation
- `config.js` — verified request email setting (blank by default)

## Before public launch
- Have the domain owner approve branding, public contact details and wording.
- Decide which pet-related activity the company will pursue.
- Configure a verified mailbox and real request submission endpoint if needed.
- Add a privacy notice before collecting or retaining customer contact details.

This is a separate exploratory project from MoveFuel.
