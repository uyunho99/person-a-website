# Person A website

Static site. No build step. Upload this whole folder to any static host (Vercel, Netlify, Cloudflare Pages, GitHub Pages, S3, or your own server). `index.html` is the entry page.

```
index.html              page, styles and scripts
assets/
  person-a-logo.png     ← add this file (see step 1)
  demo.mp4              product walkthrough, 1:49
  demo-poster.jpg       video cover image
  fonts/                Pretendard 400/500/600/700 (Latin subset, woff2)
```

## Before you deploy

1. **Logo.** Put the Person A logo at `assets/person-a-logo.png` (the file from the design system, `assets/Logo/person-a-logo.png`). Until it is added, the page shows the text "Person A" in its place.
2. **Inquiry form.** Open `index.html`, find `INQUIRY_ENDPOINT` near the bottom, and set one of:
   - `INQUIRY_ENDPOINT = "https://…"`: a form backend that accepts a JSON POST with `name`, `email`, `message` (Formspree, Basin, Getform, or your own API). Submissions are sent there.
   - `CONTACT_EMAIL = "you@person-a.ai"`: with no endpoint, the form opens the visitor's mail app with the message filled in.
   
   With neither set, the form shows "This form is not connected yet."
3. **Footer contact.** Replace `[contact email]` in the footer with your address.

## Preview locally

```
cd this-folder
python3 -m http.server 8000
```
Then open http://localhost:8000.

## Fonts

Pretendard by Kil Hyung-jin, licensed under the SIL Open Font License 1.1 (https://github.com/orioncactus/pretendard).
