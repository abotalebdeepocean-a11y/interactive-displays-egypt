# Interactive Displays Landing Page (Arabic / Egypt)

Static, mobile-responsive Arabic landing page prototype for interactive display sales. Product pricing is intentionally omitted until supplier cost and availability are confirmed.

## Files
- `index.html` — landing page and client-side event instrumentation.
- `analytics-config.js` — GA4 Measurement ID, Microsoft Clarity project ID, and business WhatsApp number.

## Analytics events
`page_view_custom`, `product_impression`, `product_view`, `select_item`, `product_quote`, `whatsapp_click`, `quote_form_start`, `generate_lead`, `quote_request_submitted`, `scroll_depth`, and CTA click events.

Personal fields (name, phone, free-text notes) are not included in analytics event parameters. Avoid sending personally identifiable information to GA4 or Clarity.

## Before production
1. Create a GA4 property and web data stream; add its Measurement ID to `analytics-config.js`.
2. Create a Microsoft Clarity project; add its project ID to `analytics-config.js`.
3. Add and verify the real business WhatsApp number in international digits.
4. The current form does not save leads to a server; it opens a WhatsApp draft only when a valid number is configured. Connect a secure server-side endpoint for reliable lead capture.
5. Confirm exact model specs, stock, supplier costs, selling prices, warranty, returns, and any delivery/installation/training services.
6. Add a privacy notice and review consent requirements before enabling analytics in production.
7. Test mobile and desktop layouts and verify analytics events.

## Deployment
Static site; connect this dedicated repository to a new Vercel project or enable GitHub Pages. Do not connect it to the existing ROVENTO project.
