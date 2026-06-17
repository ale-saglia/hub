# ale-saglia.com

Personal landing page for [ale-saglia.com](https://ale-saglia.com).

## Structure

Single static HTML file - no build step, no framework, no dependencies. CSS is inlined to keep the repo as simple as possible.

The visual style mirrors [insight.ale-saglia.com](https://insight.ale-saglia.com) - same typeface (Georgia), same colour palette, same layout width - so navigation between the two feels continuous.

## Related repositories

| Subdomain | Repository | Purpose |
|-----------|-----------|---------|
| [ale-saglia.com](https://ale-saglia.com) | this repo | Landing page |
| [insight.ale-saglia.com](https://insight.ale-saglia.com) | [ale-saglia/insight](https://github.com/ale-saglia/insight) | Technical and governance writing |
| [cv.ale-saglia.com](https://cv.ale-saglia.com) | [ale-saglia/cv](https://github.com/ale-saglia/cv) | CV as code |

## Deployment

Deployed via GitHub Pages from the `main` branch. The custom domain `ale-saglia.com` is configured via a `CNAME` file in the repo root and four `A` records pointing to GitHub's servers on Cloudflare DNS. Any push to `main` triggers a new deploy automatically. No build step required - GitHub Pages serves `index.html` directly.

## Implementation notes

**Profile image**: The profile photo is stored as `avatar.jpg` in the repo root (a copy of the GitHub profile avatar, downloaded at commit time). This removes the runtime dependency on GitHub's avatar URL, which could change or break silently. The `og:image` and `twitter:image` meta tags also point to `https://ale-saglia.com/avatar.jpg`. To update the photo, replace `avatar.jpg` with a new file and commit.