# aalto-katalogi

Static site behind **https://katalogi.aaltojuomat.fi** — the non-alcoholic catalogue for corporate gifts (FI / SV / EN), no prices.

- `/fi/` `/sv/` `/en/` — landing pages; `/?lang=xx` redirects there and keeps `utm_*`.
- `/d/xx/` — download hop: counted by Cloudflare Web Analytics (cookieless), then opens the PDF.
- `/files/Aalto_Corporate_Gifts_Catalogue_XX.pdf` — stable names; replace the file to update, links stay.
- Analytics: GA4 `G-LDGV09WVC9` (same property as aaltojuomat.fi) behind the Aalto consent banner; events `catalogue_download`, `proposal_click`, `consent_granted`. Cloudflare Web Analytics beacon on every page.

Generated — do not edit by hand. Source and build scripts: Aalto project folder `1_Aalto/6_Corporate_Gifts/3_Catalogue_PDF/src/` (`build_catalogue.py`, `render.py`, `build_site.py`).
DNS: Cloudflare zone aaltojuomat.fi, `CNAME katalogi -> malkinnick.github.io`, DNS only.
