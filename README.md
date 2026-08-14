# Hatti Moving Services — website + community posters

Plain HTML + Tailwind (CDN) + vanilla JS. No build step — open the files directly
in a browser, or upload the whole folder to any host.

## Files

| File | What it is |
|---|---|
| `index.html` | The website (one page, all sections) |
| `poster-nepali.html` | Nepali-community poster, 1080 × 1350 |
| `poster-indian.html` | Indian-community poster, 1080 × 1350 |
| `assets/logo.png` | Logo, dark version (for light backgrounds) |
| `assets/logo-white.png` | Logo, white version (for the navy sections) |

## Business details used throughout

- Phone — **(605) 659-4528** (`tel:+16056594528`)
- Email — **info@hattimovingservice.com**
- Calendly — https://calendly.com/wasdthedebugger/talk-to-nikas
- Area — D.C., Maryland & Virginia (DMV)
- Footer — A Icuwan Venture · www.icuwan.com

All three came from the existing business card, so they match your print material.

## The opening-sale section (currently OFF)

Each of the three files has a promo block that is **commented out**, as asked.
To switch it on, delete the two marker lines around it:

```
<!--  START PROMO  ▼▼▼          ← delete this line
   ...the promo markup...
END PROMO  ▲▲▲  -->             ← and this line
```

Before going live, replace the placeholders inside: the discount `20%`,
the expiry `[END DATE]` / `[मिति]` / `[तारीख]`, and the code `HATTI20`.

Both layouts were checked with the promo on and off — nothing overflows either way.

## Exporting the posters

Open a poster file and click **Download PNG** — it saves at full 1080 × 1350
regardless of your screen size. **Print** → *Save as PDF* is the fallback.
The download button needs an internet connection (it loads html2canvas); a
screenshot works offline.

## Quote form

There is no backend, so the form opens the visitor's mail app with every field
pre-filled and addressed to info@hattimovingservice.com. To switch to a real
endpoint (Formspree, Netlify Forms, your own API), replace the body of the
submit handler at the bottom of `index.html` with a `fetch()` POST — the comment
there marks the spot.

## Notes

- Stats in the hero (500+ moves, 4.9★) and the three reviews are **placeholders**
  — swap them for real numbers and real customer quotes before launch.
- Tailwind loads from the CDN, which shows a console warning in production. For a
  real deployment, run the Tailwind CLI once and link the generated CSS instead.
