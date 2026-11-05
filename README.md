# Colab Cola website

Minimal static website for https://colabcola.com — GitHub Pages, no JavaScript or tracking scripts.

## Structure

- `index.html` — homepage
- `privacy/index.html` — Google OAuth privacy policy
- `docs/index.html` — getting started guide
- `assets/site.css` and `assets/colabcola-banner.png` — styling and approved banner
- `CNAME` — `colabcola.com`

## Publishing

Create a **separate public** GitHub repository `dependanz/colabcola-site` and push these files to `main`. Under **Settings → Pages**, select **Deploy from a branch**, `main`, `/(root)`, then set the custom domain `colabcola.com`. Do this BEFORE changing DNS.

At Squarespace DNS, create A records on `@` pointing to GitHub Pages' documented addresses:

```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

Optionally add a `www` CNAME pointing to `dependanz.github.io` (no `https://`). Preserve any existing MX/TXT email records; only replace conflicting apex/`www` web records. Avoid wildcard DNS. Enable HTTPS in GitHub Pages once the certificate is provisioned.

## Before publishing publicly

Review the privacy policy for accuracy against current implementation and confirm the support email may be displayed publicly. The website does not include app credentials or OAuth tokens. Branding must not imply affiliation with Google. Google OAuth production approval and domain verification are separate processes.

Current code repository is private; the website is intentionally independent. After public release, add a link to the code repository and update any provisional language about PyPI availability.
