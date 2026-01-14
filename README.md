# The Simple Magazine

An ultra-minimal magazine website for GitHub Pages. Zero build process, zero automation, just HTML files.

## Quick Start (5 Minutes)

1. **Fork or clone this repository**
2. **Enable GitHub Pages:**
   - Go to Settings → Pages
   - Source: Deploy from a branch
   - Branch: `main` / `root`
   - Save
3. **Your site is live!** Visit `https://YOUR-USERNAME.github.io/YOUR-REPO/`

That's it. No configuration needed.

## File Structure

```
├── index.html              # Homepage (article list)
├── style.css               # All styling for the entire site
├── article-template.html   # Copy this to create new articles
├── submit.html            # Contact/submission page
└── articles/              # All articles go here
    ├── welcome.html
    └── example-article.html
```

## How to Publish a New Article (2 Minutes)

### Step 1: Create Your Article

1. Copy `article-template.html`
2. Open it in any text editor
3. Change the `<title>` tag
4. Replace the content with your article
5. Save it as `articles/your-article-name.html`

**Naming convention:** Use lowercase with hyphens: `my-great-article.html`

### Step 2: Add to Homepage

1. Open `index.html`
2. Find the comment: `<!-- ADD NEW ARTICLES HERE -->`
3. Copy one of the existing article preview blocks
4. Update it with your article's details:

```html
<article class="article-preview">
    <h2><a href="articles/your-article-name.html">Your Article Title</a></h2>
    <p class="meta">January 14, 2026 • Your Name</p>
    <p>Brief description or first sentence.</p>
</article>
```

5. Place it at the TOP (newest articles first)

### Step 3: Commit and Push

```bash
git add .
git commit -m "Add new article: Your Article Title"
git push
```

Your article is live in ~30 seconds!

## HTML Tags You Can Use

In articles, you can use standard HTML:

- `<p>` - Paragraphs
- `<h2>`, `<h3>` - Headings (h1 is the article title)
- `<ul>`, `<ol>`, `<li>` - Lists
- `<blockquote>` - Quotes
- `<code>` - Inline code
- `<pre><code>` - Code blocks
- `<a href="">` - Links
- `<em>`, `<strong>` - Emphasis
- `<img src="" alt="">` - Images (place in `/images/` folder)

The CSS automatically styles everything. No classes needed.

## Customization

### Change Colors/Fonts

Edit `style.css` at the top:

```css
body {
    font-family: Georgia, 'Times New Roman', serif;
    color: #222;
    background: #fff;
}
```

### Change Site Name

1. Edit the `<h1>` in `index.html`, `article-template.html`, and all article files
2. Or do a find-and-replace across all files

### Add Images

1. Create an `images/` folder in the root
2. Place your images there
3. Reference them in articles:

```html
<img src="../images/your-image.jpg" alt="Description" style="max-width: 100%;">
```

### Update Submit Page

Edit `submit.html` and replace:
- `editor@yourmagazine.com` with your email
- `YOUR-USERNAME/YOUR-REPO` with your GitHub repository URL

## What This Doesn't Do

- No search functionality
- No tags or categories
- No RSS feed (unless you manually create one)
- No comment system
- No analytics (add Google Analytics if needed)
- No automatic article discovery
- No fancy admin interface

**If you need these features, this isn't the right tool.**

## Advanced: Optional Additions

### Add Google Analytics

Add before `</head>` in all HTML files:

```html
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

### Add RSS Feed

Create `feed.xml` manually and update it when you add articles.

### Add Custom Domain

1. Add a `CNAME` file in the root with your domain
2. Configure DNS at your domain provider
3. See [GitHub's custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)

## Philosophy

This system is intentionally minimal. It's for people who:

- Value simplicity over features
- Are comfortable editing HTML
- Want complete control
- Don't need a CMS
- Prefer transparency to magic

Modern web publishing has become unnecessarily complex. This is a return to basics.

## License

Public domain / CC0. Do whatever you want with this.

## Support

This is a template, not a product. There's no support, no updates, no roadmap. Fork it and make it yours.

## Credits

Built with pure HTML and CSS. No frameworks, no dependencies, no build process.
