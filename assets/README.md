# J.L. Coe Painting Website
Production-ready static site for J.L. Coe Painting built with vanilla HTML, CSS, and JavaScript. The layout is mobile-first, accessible, and ready to deploy on GitHub Pages.
## Quick Start
- **Preview locally** with a simple static server (instructions below).
- **Update contact details** and Formspree endpoint in `index.html`.
- **Deploy** by pushing to GitHub and enabling Pages on the `main` branch.
## Local Preview
Choose one of the lightweight options:
- **VS Code Live Server:** Right-click `index.html` and select “Open with Live Server”.
- **Python 3:** Run `python -m http.server 8080` from the project root, then visit `http://localhost:8080`.
## Editing Content
All site content lives inside `index.html`.
1. **Contact details:** Update the email (`lee@jlcoepainting.com`), phone numbers, and service area text in the hero and contact sections.
2. **Hero & gallery images:** `index.html` ships with inline SVG placeholders so the layout works even without photography. Replace each `<img>` `src` with your production-ready asset (local file path, CDN URL, etc.) while keeping the descriptive `alt` text accurate.
3. **Brand colors:** Modify the CSS variable `--brand` near the top of the `<style>` block to adjust the gold accent shade.
4. **Structured data:** Update the JSON-LD block in the `<head>` if business details change.
## Contact Form (Formspree)
1. Create a free Formspree account at [https://formspree.io](https://formspree.io).
2. Add a new form and copy the Form ID (format looks like `https://formspree.io/f/abcd1234`).
3. In `index.html`, replace `YOUR_FORM_ID` in the `action` attribute of the contact form with your actual Form ID.
4. Submit a test message from the live site and verify the confirmation email sent by Formspree.
5. Optionally customize autoresponses or spam protection from your Formspree dashboard.
## Deployment (GitHub Pages)
1. Create a new GitHub repository and commit all files from this project root.
2. Push to GitHub and open the repository settings.
3. Under **Pages**, choose the `main` branch with the `/ (root)` folder and save.
4. GitHub Pages will publish your site at `https://<username>.github.io/<repo>/` within a few minutes.
## Custom Domain (Optional)
1. Edit the `CNAME` file to contain your custom domain, e.g. `www.jlcoepainting.com`.
2. In your DNS provider, create the following records:
   - `A` records pointing `@` to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`.
   - `CNAME` record pointing `www` to `<username>.github.io`.
3. In GitHub Pages settings, add your custom domain and enforce HTTPS.
## File Map
```
.
├─ index.html        # Main site markup, styles, and JavaScript
├─ assets/
│  └─ README.md      # Project documentation (this file)
└─ .gitignore        # Common development ignores
```
