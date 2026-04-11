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
| cv.ale-saglia.com | ale-saglia/cv *(planned)* | CV |

## Deployment

Deployed via GitHub Pages from the `main` branch. The custom domain `ale-saglia.com` is configured via a `CNAME` file in the repo root and four `A` records pointing to GitHub's servers on Cloudflare DNS. Any push to `main` triggers a new deploy automatically. No build step required - GitHub Pages serves `index.html` directly.

## Implementation notes

**Profile image**: The profile photo is sourced dynamically from `https://github.com/ale-saglia.png` - the publicly available avatar image from this GitHub profile. This is a conscious design choice: the avatar stays in sync with any GitHub profile updates automatically, without requiring manual synchronization. The trade-off is an external dependency on GitHub's avatar service.