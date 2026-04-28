# mono-pitch

An opinionated single-page site template. Mono-spaced, hairline-ruled, no JS framework, no build step. Designed for personal pitch / application sites, but the structure works for any opinionated single-page thing — manifestos, product memos, project intros, course pages.

**Live demo:** [romecar.github.io/mono-pitch](https://romecar.github.io/mono-pitch/)

## What's in the box

| File | Purpose |
|---|---|
| `index.html` | Rendered demo (fictional candidate, fictional company). What GitHub Pages serves. |
| `template.html` | Same design with every customizable bit replaced by `[BRACKETS]`. Start here when you fork. |
| `LICENSE` | MIT. |

## Why it works

- **Mono font + hairline rules** signals craft without noise. JetBrains Mono throughout. White background, black text, one inverted footer block. No accent colour.
- **Numbered sections** read like a memo, not a CV. The reader knows where they are.
- **Hero is one defensible sentence.** Opinionated tagline, then a single line of context. The whole page can be skimmed in twenty seconds and the thesis lands.
- **POV section** is what most personal sites lack. Saying something defensible about the actual problem the page exists to discuss is the strongest signal of substance.
- **Track-record table** is the most efficient way to answer "do you have the experience" — requirement on the left, specific evidence on the right.
- **Inverted footer** breaks the visual rhythm and gives the contact block weight.

## Section structure

| § | Section | What goes here |
|---|---|---|
| 01 | **POV** | Your sharp, defensible opinion on the problem. Demonstrates you've thought about the work, not just the application. |
| 02 | **Track record** | Requirement on the left, specific evidence on the right. Numbers help. |
| 03 | **Craft** | If you're a heavy user of what they make, prove it with numbers. Delete the section otherwise. |
| 04 | **Why** | Personal, defensible, names concrete things. Not a mission statement. |
| 05 | **References** | Names + titles. "Introductions on request." |
| 06 | **Contact** (footer) | Inverted black block. Email, LinkedIn, downloads. |

## Quick start

```bash
git clone https://github.com/RomeCar/mono-pitch.git
cd mono-pitch

# Use template.html as your starting point — replace every [BRACKET]
cp template.html my-site.html
# Open my-site.html in an editor, replace [YOUR NAME], [COMPANY], etc.
# Drop your CV PDF as cv.pdf

# Deploy anywhere static:
#   - Netlify: drag the folder into netlify.com/drop
#   - Vercel: vercel deploy
#   - GitHub Pages: push to gh-pages branch
#   - Caddy / nginx / S3+CF: copy to docroot
```

## Customization tips

- **Reorder sections freely.** Each `<section>` is self-contained.
- **Drop §03 (Craft)** if you're not a heavy user of the thing the page is about. Empty stat cards read as filler.
- **Keep the page short.** The whole point is one screen of POV + one screen of evidence. Adding more sections dilutes signal.
- **Stat cards work best with concrete units.** "47 workspaces / 2 years" beats "expert level". Specific numbers are more credible than adjectives.
- **The hero tagline is the most important line on the page.** A defensible thesis the reader will remember even if they skim the rest.
- **Two fonts max.** The template uses one (JetBrains Mono). Adding a serif for the headlines is fine, but resist the urge to add more.

## License

MIT. Use it, fork it, strip the credit. If you ship something nice with it, open a discussion — I'd love to see.

## Credits

Design inspired by [Ollama](https://ollama.com/) — the mono aesthetic, the generous whitespace, the lack of accent colour.
Typography: [JetBrains Mono](https://www.jetbrains.com/lp/mono/).
CSS: [Tailwind](https://tailwindcss.com/) via CDN.
