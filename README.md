# Feature Rich Software — Full-Stack Software Consulting Landing Page

A beautiful, production-ready single-file landing page for Feature Rich Software, a full-stack software consulting company that builds everything from modern UIs to resilient cloud infrastructure.

## Features

- **Modern, premium design** — Dark theme with elegant indigo/cyan accents and refined typography
- **Fully responsive** — Perfect on desktop, tablet, and mobile
- **Interactive elements**:
  - Mobile hamburger menu
  - Testimonial carousel (auto-rotating + manual controls)
  - Detailed case study modals
  - Working contact form with success states
- **Truly static & self-contained** — Main file is `index.html` + `logo.png` (the brand mark). Designed for easy deployment to GitHub Pages, Vercel, Netlify, Cloudflare Pages, S3, etc.
- **Mobile-first design** — Quality experience on both mobile and desktop. All future changes will follow this principle.
- **Easy to customize** — Clear structure and comments throughout

## Quick Start

1. Open `index.html` directly in any browser (double-click works)
2. Or serve it locally:

```bash
# Using Python
python3 -m http.server 8080

# Using npx
npx serve .
```

3. Visit `http://localhost:8080`

## Responsiveness

The site is built mobile-first. It delivers a high-quality experience on phones, tablets, and desktop. The navbar, grids, typography, and spacing all adapt intelligently.

## Deploying to GitHub Pages (Recommended)

This site is intentionally built as a single static HTML file so it's trivial to host on GitHub Pages.

### Steps:

1. **Create a new repository** (or use an existing one) on GitHub.
2. **Add these files** to the root of the repo:
   - `index.html`
   - `logo.png` (the official brand mark used in the navbar and as the favicon)
   - (Optional) `README.md`
3. **Create an empty `.nojekyll` file** in the root (this prevents GitHub from processing the site with Jekyll).
4. Go to **Settings → Pages** in your repository.
5. Under "Build and deployment", set **Source** to "Deploy from a branch".
6. Choose the `main` branch and `/ (root)` folder.
7. Click **Save**.

Your site will be live at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

**Pro tips:**
- Use a custom domain? Just add a `CNAME` file with your domain.
- Want the cleanest URLs if you ever add more pages? The `.nojekyll` file handles that.
- For even fewer external dependencies later, you can replace the Tailwind Play CDN and Font Awesome with inlined CSS (the current setup already works reliably on GitHub Pages).

## Deploying Elsewhere

The same `index.html` works great on:
- **Vercel** — Drag & drop the folder (or connect the repo)
- **Netlify** — Same
- **Cloudflare Pages** — Excellent performance
- **AWS S3 + CloudFront** or **Render**

## Customization Guide

### 1. Company Identity & Logo (top of file)

- **Logo**: The official logo is provided as `logo.png` in the project root. It is used in the navbar and as the favicon.
- **Wordmark text**: "Feature Rich Software" appears next to the logo in the navbar (larger size, clean system font).
- **Contact email**: `hello@featurerich.dev`
- **Location text**: San Francisco + remote hubs
- **Social links**: Currently point to `#` (X/Twitter, LinkedIn, GitHub)

### 2. Hero & Messaging

- Main headline: line ~95
- Subheadline: line ~99
- Trust badges and hero visual are easy to tweak visually

### 3. Services / Capabilities

Six service cards starting around line 160. Each card has:
- Icon (Font Awesome class)
- Title
- Description
- Tech pills

### 4. Case Studies

Data lives in a clean JavaScript array (`caseStudies`) near the bottom of the script. Update the three objects to match your real projects. The modal rendering is automatic.

### 5. Testimonials

Three testimonials defined in the HTML. Swap quotes, names, and the avatar styles (currently self-contained CSS gradient circles with initials — no external images).

### 6. Contact Form

Currently shows a success toast. To make it actually send emails:

**Recommended options:**

- **Formspree** (easiest): Add `action="https://formspree.io/f/YOUR_ID"` and `method="POST"` to the `<form>` tag
- **Netlify Forms**: Add `netlify` attribute if deploying to Netlify
- **Web3Forms** or **EmailJS** for more control

### 7. Colors & Branding

Primary accent is indigo-500 (`#6366f1`) with cyan-400 secondary. Change the `.gradient-text` class easily for the headline accent.

## Deployment Options

All of these support static sites (include both `index.html` and `logo.png` when deploying):

| Platform       | Difficulty | Notes                              |
|----------------|------------|------------------------------------|
| **Vercel**     | Trivial    | Drag & drop the folder             |
| **Netlify**    | Trivial    | Drag & drop the folder or connect repo |
| **GitHub Pages** | Easy     | Push `index.html` + `logo.png` to a `gh-pages` branch |
| **Cloudflare Pages** | Easy | Excellent performance              |
| **AWS S3 + CloudFront** | Medium | Fully custom domain + CDN       |
| **Render**     | Easy       | Static site hosting                |

**Pro tip**: For the absolute best performance and global CDN, deploy to Vercel or Cloudflare Pages. Remember to include both `index.html` and `logo.png`.

## Going Further

If you later want a more advanced setup:

- Convert to a proper **Next.js** or **Astro** project (great for blogs + multiple pages)
- Add **TypeScript** + componentization
- Integrate real analytics (Plausible, PostHog, or GA4)
- Add a blog using MDX or Sanity

## License

Free to use and modify for your own business. Just update the company name/details before publishing.

---

Built with care for ambitious engineering teams. Questions or need help customizing? Open an issue or just edit the file — it's intentionally simple.

Enjoy the launch. 🚀
