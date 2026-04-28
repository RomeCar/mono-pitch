# mono-pitch

A single-page application site for landing the job. Mono-spaced, opinionated, no JS framework, no build step.

Built originally for [one specific application](https://anthropic.zerocommoditiestrading.com) (a senior commercial role at an AI lab). Released as a template because the structure turned out to be more useful than the original content.

## What it is

One HTML file. Drop it on any static host. Customize by replacing everything in `[BRACKETS]`.

The site is structured as **six numbered sections** that map to what a hiring committee actually wants to know:

| § | Section | What goes here |
|---|---|---|
| 01 | **POV** | Your sharp, defensible opinion on the problem the role exists to solve. Demonstrates you've thought about the work, not just the job. |
| 02 | **Track record** | The JD's "you may be a good fit if..." bullets, each mapped to one specific piece of evidence. |
| 03 | **Product / craft** | If you're a heavy user of what the company makes, prove it with numbers. Delete the section otherwise. |
| 04 | **Why this company** | Personal, defensible, names concrete things they've done. Not their mission statement. |
| 05 | **References** | Names + titles. "Introductions on request." |
| 06 | **Contact** (footer) | Inverted black block for visual rhythm. Email, LinkedIn, downloads. |

A hero section at the top carries the one-line tagline, and a thin top nav with anchor jumps lets a busy reader skip around.

## Why it works

- **Mono font + hairline rules** signals craft without noise. JetBrains Mono throughout. White background, black text, one inverted footer block. No accent colour.
- **Numbered sections** read like a memo, not a CV. The reader knows where they are.
- **Track-record table** is the most efficient way to answer "do you have the experience" — JD requirement on the left, your specific evidence on the right.
- **POV section** is what most application sites lack. Saying something defensible about the actual problem the role exists to solve is the strongest signal of fit.
- **No build step** — it's a single HTML file with Tailwind via CDN. You can deploy it in 60 seconds.

## Quick start

```bash
git clone https://github.com/RomeCar/mono-pitch.git
cd mono-pitch

# Edit index.html — replace every [BRACKET] with your content
# Drop your CV PDF in the same folder as cv.pdf

# Deploy anywhere static:
#   - Netlify: drag the folder into netlify.com/drop
#   - Vercel: vercel deploy
#   - GitHub Pages: push to gh-pages branch
#   - Caddy / nginx: copy to docroot
#   - S3 + CloudFront: aws s3 sync
```

## Customization tips

- **Don't keep section §03 (Product/craft)** unless you're genuinely a heavy user of the company's product. Empty stat cards read as filler.
- **Reorder sections freely.** Each `<section>` is self-contained.
- **Keep the page short.** The whole point is one screen of POV + one screen of evidence. Adding more sections dilutes signal.
- **The number stat cards in §03 work best with concrete units.** "366 PRs / 30 days" beats "expert level". "1.2 GW originated" beats "extensive experience".
- **The hero tagline is the most important line on the page.** It should be a defensible thesis the reader will remember even if they skim everything else. "For AI in Europe, the deal is power" — that kind of thing.

## Optional: password-gate it

If you want to share the site with a recruiter without indexing it publicly, the original deployment used a tiny Python auth server behind Caddy. The auth code isn't in this repo (it's deployment-specific), but the pattern is: serve `index.html` only when the request carries a valid auth cookie; otherwise redirect to a login page. ~100 lines of stdlib Python is enough.

If there's interest, open an issue and I'll factor it out.

## License

MIT. Use it, fork it, strip the credit. If you land the job because of it, I'd love to hear about it (open an issue / discussion).

## Credits

Design inspired by [Ollama](https://ollama.com/) — the mono aesthetic, the generous whitespace, the lack of accent colour. Typography: [JetBrains Mono](https://www.jetbrains.com/lp/mono/). CSS: [Tailwind](https://tailwindcss.com/) via CDN.

Built by [Rommero Carrillo](https://github.com/RomeCar) over the course of one job application.
