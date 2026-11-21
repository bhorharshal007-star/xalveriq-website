# Xalveriq website

One-page website for **Xalveriq**: done-for-you business automation (WhatsApp + CRM + AI follow-up systems) and booking-ready websites for coaching institutes, clinics, dental clinics, real estate agencies, CA firms and recruitment agencies.

Plain HTML, CSS and a little JavaScript in a single file. No build step, no dependencies. All animations are CSS and SVG.

## Files

- `index.html`: the whole site (sections, styles, scripts)
- `assets/`: logo and favicon
- `vercel.json`: static hosting headers
- `Xalveriq-services-prompt.md`: services, pricing and the prompt used to brief the Services section

## Contact settings

At the bottom of `index.html`, edit the `CONFIG` block:

```js
const CONFIG = {
  whatsapp: "919370461591",  // digits only, with country code
  phone: "+919370461591",
  webhook: ""                // optional: n8n / Make / Zapier webhook URL
};
```

The contact form opens WhatsApp with every field pre-filled. If you set `webhook`, each submission is also POSTed to that URL as JSON, so a workflow can forward leads to you automatically.

## Run locally

```bash
npx serve .
```

## Deploy

Hosted on Vercel as a static site:

```bash
npx vercel deploy --prod
```
