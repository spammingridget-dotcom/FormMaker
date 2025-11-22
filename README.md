# Simple Static Form Builder (Web3Forms)

This repository contains a tiny static form-builder that produces HTML forms which submit to Web3Forms (no backend required). Use GitHub Pages to host the produced HTML on your own domain.

## How it works
- Open `index.html` (the builder) in your browser (localhost or GitHub Pages).
- Add fields, reorder with drag & drop, set a form name and optionally a recipient email.
- Click **Export** to open the generated `form.html` in a new tab, or **Download** to save the HTML file.
- The generated HTML contains your Web3Forms access key and will POST directly to Web3Forms.

## Deploying to GitHub Pages
1. Create a new GitHub repository and push these files.
2. In repository settings → Pages, set the source to the `main` branch (root) or the `docs/` folder.
3. Wait a minute and open `https://<your-username>.github.io/<repo-name>/index.html`
4. Open the builder, create a form and **Download** the generated HTML. Upload the generated file (`form.html`) to the same repo or serve it from the repo root.

## Security notes
- This approach embeds a Web3Forms access key into a static HTML file. That is how Web3Forms is designed; the key allows Web3Forms to know which account receives emails.
- If you share the HTML publicly, treat the access key as visible. If you need better control, use a server-side proxy or protected webhook.

## Support
If you want:
- An automated GitHub Pages workflow that deploys the generated `form.html` directly into the `docs/` folder, I can add it.
- A version that stores forms in a repo automatically (via GitHub Actions), I can add that too.

Enjoy!
