# ClickFunnels public-route fix

The deployed `/affiliate-funnel` page was showing the internal five-entry Affiliate Funnel OS demo. The approved production journey is now `/affiliate-funnel` (lean Funnel Validation Playbook lead capture) and `/affiliate-funnel/ready` (ready-buyer page with the three approved objections and ClickFunnels CTA).

Deploy the latest `main` commit. Keep `/api/leads`, `/api/events`, the database, tags, and email sequence wiring. Set production values in the host environment (never commit secrets): `AFFILIATE_URL_THREE_MONTHS`, `RESEND_API_KEY`, `LEAD_FROM_EMAIL`, `META_PIXEL_ID=1679259859838157`, and `META_CAPI_ACCESS_TOKEN`.

After deployment, verify both routes on mobile and submit one controlled test lead. Confirm storage, email/PDF delivery, browser `Lead`, accepted server-side Meta event, and the ready-buyer CTA URL. Do not expose the other placeholder offers on the public entry page.
