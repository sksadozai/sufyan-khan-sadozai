# Sufyan Khan Sadozai — Personal Article Publication

A bilingual (English and Urdu) personal writing website built with plain HTML, CSS, and JavaScript. It is designed for free hosting on GitHub Pages.

## Website structure

```text
.
├── index.html              # Homepage
├── articles.html           # Article listing, search, and category filter
├── article.html            # Individual article view
├── about.html              # Author introduction
├── assets/
│   ├── css/style.css       # Editorial visual design
│   └── js/site.js          # Article data and site interactions
└── README.md
```

## Preview locally

You can open `index.html` directly in a browser. For a local web server, run:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Publish with GitHub Pages

1. Create a new **public** GitHub repository named exactly `sufyankhansadozai.github.io` (if that username is available and is your actual GitHub username).
2. Extract these website files and upload the contents to the repository root. `index.html` must be at the root, not inside another folder.
3. Commit the files to the `main` branch.
4. In the repository, open **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/(root)`, then save.
6. Wait for GitHub Pages to publish. Your site address will be `https://YOUR-GITHUB-USERNAME.github.io/`.

If your GitHub username is different, use that exact username in the repository name and URL.

## Add a new article

Open `assets/js/site.js`. Add another article object to the `articles` array. Each article needs:

- `id`: unique lowercase URL slug, e.g. `the-value-of-patience`
- `title`: article title
- `category`: `Self-discovery`, `Society`, or `Life lessons`
- `date`: publication date
- `language`: language label
- `excerpt`: short summary
- `en`: English content blocks
- `ur`: Urdu content blocks

Content blocks use:
- `["p", "Paragraph text"]`
- `["h2", "Section heading"]`
- `["quote", "A highlighted quotation"]`

Use `article.html?id=your-article-id` as the article URL. The homepage and article listing update automatically.

## Custom domain later

You can keep GitHub Pages hosting and connect a domain you buy later. In the repository, open **Settings → Pages → Custom domain**, enter your domain, and follow GitHub's DNS instructions at your domain registrar. Do not purchase a separate hosting package unless you specifically need features GitHub Pages cannot provide.

## Before publishing

- Review the author bio and decide whether you want to show an email or social links.
- Check spelling, punctuation, and Urdu rendering on your phone.
- Replace the sample article text if you want to publish a revised final version.
- Add a favicon and social sharing image later if desired.

## Notes

This is a static website: it has no admin dashboard or database. You publish by editing `assets/js/site.js` and pushing the changes to GitHub. It uses Google Fonts when an internet connection is available; fallback fonts are included.
