# Scrapyard Brawl site (privacy, support, holding page)

Static, no build step. `index.html` (holding page), `privacy.html`, `support.html`, `style.css`.
Fonts are the game's own OFL fonts (Bangers display, Rubik body). Colors are the game's UI tokens.

## Before publishing

1. Replace every `[[OPERATOR]]` (legal name of the developer or company) and `[[EMAIL]]` (support inbox):
   `grep -rn '\[\[' site/` must print nothing.
2. The privacy policy makes promises the ad integration must keep: see `game/docs/store/APPLE_HANDOFF.md` §A6.2.
3. Preview locally: `cd site && python3 -m http.server 8743`, then open http://localhost:8743.

## Hosting

The pages are commercial (they support a paid app), so **not Vercel Hobby**: its free tier is
non-commercial only. Free options that allow commercial use:
- **GitHub Pages** from a small *public* repo holding only `site/` (free Pages needs a public repo).
- **Cloudflare Pages** (free tier allows commercial use).

The App Store and Play Console need: Privacy Policy URL = `<host>/privacy.html`, Support URL = `<host>/support.html`.

## Later

`index.html` is a holding page. The real marketing landing page (store badges, trailer, screenshots) should be
designed with the full `web-design` process once the clean-room art is finished.
