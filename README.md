# Principles Analytics — Website

Static website for [principles-analytics.com](https://www.principles-analytics.com), hosted on GitHub Pages.

## Structure

```
├── index.html        Home page
├── about.html        About page
├── contact.html      Contact page
├── css/
│   └── style.css     Shared stylesheet
├── assets/
│   └── favicon.svg   Site favicon
└── CNAME             Custom domain for GitHub Pages
```

## Deployment (GitHub Pages)

1. Push this repository to GitHub.
2. Go to **Settings → Pages**.
3. Set **Source** to `main` branch, root folder `/`.
4. GitHub will automatically detect the `CNAME` file and configure `www.principles-analytics.com`.

## Custom domain (Namecheap)

Add the following DNS records in Namecheap:

| Type  | Host | Value                        |
|-------|------|------------------------------|
| CNAME | www  | `<your-github-username>.github.io` |
| A     | @    | `185.199.108.153`            |
| A     | @    | `185.199.109.153`            |
| A     | @    | `185.199.110.153`            |
| A     | @    | `185.199.111.153`            |

These `A` records point the apex domain (`principles-analytics.com`) at GitHub's servers.
DNS propagation typically takes a few minutes to a few hours.

## Contact form

The contact form uses [Formspree](https://formspree.io) (free tier: 50 submissions/month).

1. Sign up at formspree.io.
2. Create a new form → copy your form endpoint ID.
3. In `contact.html`, replace `YOUR_FORM_ID` with your actual ID:
   ```html
   action="https://formspree.io/f/YOUR_FORM_ID"
   ```

## Personalisation checklist

- [ ] Update email address in `contact.html`
- [ ] Update LinkedIn URL in `contact.html`
- [ ] Update location in `contact.html`
- [ ] Set up Formspree and replace `YOUR_FORM_ID`
- [ ] Review and personalise the About page bio
- [ ] Replace `CNAME` content if your domain differs from `www.principles-analytics.com`
