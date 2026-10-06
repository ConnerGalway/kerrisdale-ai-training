# Kerrisdale Lumber Brand Guide

**For:** the Kerrisdale Lumber x Junction Consulting AI Accelerator dashboard
**Source:** a review of kerrisdalelumbercd.ca (Home and About pages, saved HTML and screenshots), October 2026
**Status:** colours were sampled from screenshots, and fonts were taken from the site's code. Kerrisdale hasn't supplied official brand standards, so confirm with Lyle before anything client-facing goes to print.

> **Note for Claude Code:** this file replaces the placeholder palette (timber green, wood tan, charcoal) in the original build brief. Use the tokens in section 8.

---

## 1. Brand at a glance

| | |
|---|---|
| **Full name** | The Kerrisdale Lumber Company |
| **Short name** | Kerrisdale Lumber (in body copy, never shortened to "KL") |
| **Founded** | 1921 ("Est. 1921" is part of the logo) |
| **Division name on the site** | Kerrisdale Lumber Contractor Division |
| **Location** | 1253 West 76th Ave, Vancouver, BC |
| **Who they serve** | Vancouver general contractors and home builders, from single homes to multi-family wood frame |
| **Brand idea** | A century-old, family-run yard that works like a modern project partner |
| **Site headline** | "We Deliver What You Need, When You Need It." |
| **About page headline** | "Built on Tradition, Driven by Innovation" |

The site is almost entirely black and white. It has no accent colour. The look comes from archival black-and-white photography, an engraved heritage logo and classic serif type. Keep the dashboard in that world: dark, calm, typographic and confident.

---

## 2. Logo

**What it is:** a hand-engraved illustration of a man walking beside a horse pulling a lumber cart. Below it is a stacked wordmark in engraved capitals:

```
— THE —
KERRISDALE
LUMBER
COMPANY
────────
EST. 1921
```

**Files**
- `kerrisdale-logo-white.webp` (in this repo): a white logo on a transparent background, 1000 x 1000px. Use it on black or dark charcoal only.
- The site also uses `KL Company - Black Background.png` (1500 x 1500) as its social share image. Ask Lyle for the original vector (SVG, EPS or AI) and a black-on-transparent version.

**Usage**
- Always place it on black (`#000000`) or Slate (`#20242A`). The engraved line work disappears on light or busy backgrounds.
- Centre it in headers, as the website does. The navigation sits on the left and the call to action on the right.
- **Minimum size:** 96px wide on screen. Below that, "COMPANY" and "EST. 1921" can't be read. On a phone header, use 80 to 96px.
- **Clear space:** leave at least the height of the "THE" line on every side.
- **Don't:**
  - recolour it, add effects or outlines
  - crop the horse and cart away from the wordmark
  - stretch it
  - set it over photography without a dark overlay
- **Dashboard embedding:** base64-encode the WebP into the `LOGO_B64_HERE` placeholder (`data:image/webp;base64,...`). Add alt text: "The Kerrisdale Lumber Company, Est. 1921".

---

## 3. Colour

The site palette is monochrome. These values were sampled from the live site.

| Token | Hex | Where it appears on the site | Dashboard use |
|---|---|---|---|
| **Yard Black** | `#000000` | Page background, header, most sections | Page background, header |
| **Slate** | `#20242A` | The darkened photo overlay behind the testimonial and quote band | Cards, panels, table headers, the tab bar |
| **Silver** | `#DCDCDC` | "Get a Quote" pill button, large quote text | Primary buttons, active tab, emphasis text |
| **Paper White** | `#FAFAFA` | Headings ("Visit Us", "Our Story") | Headings, the logo, key numbers |
| **Ash** | `#B8B8B8` | Secondary body text | Body text on black |
| **Steel** | `#808080` | Muted labels and dividers | Captions, metadata, borders at 40% opacity |

**Contrast** (all pass WCAG AA for body text on Yard Black)
- Paper White 20.1:1
- Silver 15.3:1
- Ash 10.6:1
- Steel 5.3:1, so use it only for small labels, not long paragraphs

On Slate, Ash is 7.9:1 and passes. Steel is only 3.9:1 on Slate, so don't use Steel for text on cards. Use Ash there instead.

**Functional colours (dashboard only, not from the site)**

The site has no status colours, but the dashboard needs a few. Keep them muted so they sit quietly in the monochrome system:
- Complete: `#7FA383` (muted sage)
- In progress: `#C9A66B` (aged brass)
- Upcoming: Silver outline with no fill

Use them only for small badges, ticks and the progress bar. Never use them as section backgrounds.

---

## 4. Typography

These are taken from the site's code. Both fonts are free on Google Fonts.

| Role | Font | Notes |
|---|---|---|
| **Display and headings** | **Gilda Display** (regular 400) | An elegant, high-contrast serif. It's used large and in title case: "Our Story", "Visit Us", "Built on Tradition, Driven by Innovation". It only comes in one weight, so build hierarchy with size, not bold. |
| **Body, navigation and buttons** | **PT Serif** (400, 400 italic, 700) | A warm, readable serif. It's used for paragraphs, nav links, the "Get a Quote" button and attributions. |
| **Labels and data** (dashboard addition) | IBM Plex Mono (400, 500) | Kept from the Twin Lions system for eyebrows, dates and session numbers. Use it in uppercase with letter spacing around 0.08em. |

```html
<link href="https://fonts.googleapis.com/css2?family=Gilda+Display&family=PT+Serif:ital,wght@0,400;0,700;1,400&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">
```

**Scale for the dashboard** (desktop, then mobile)

| Element | Desktop | Mobile |
|---|---|---|
| Hero H1 | Gilda Display, 56px | 36px |
| H2 | 36px | 28px |
| H3 | 24px | 21px |
| Body | PT Serif, 18px, line height 1.6 | 17px |
| Labels | Plex Mono, 12 to 13px | Same |

Headings use title case, like the site. Don't set Gilda Display in all caps, because it loses its character. The engraved capitals belong to the logo only.

---

## 5. Layout and components

These patterns were observed on the site. Carry them into the dashboard.

- **Header:** black. Nav links sit on the left in PT Serif, with the active link marked by a thin underline. The logo is centred, and the call to action sits on the right. For the dashboard, the tab bar can sit directly under this header, still on black.
- **Buttons:** fully rounded pills (border radius 999px), filled with Silver and set in Yard Black PT Serif at about 18px. They have generous horizontal padding (around 40px) and no shadow. Secondary buttons use a Silver 1px outline on a transparent background.
- **Sections:**
  - full-width black bands with plenty of vertical space (100px or more on desktop)
  - feature panels in Slate
  - the About page uses a soft curved divider between the hero photo and the content, which can be echoed on the hero once
- **Photography:**
  - archival black-and-white images of the original 1920s storefront, and present-day yard photos
  - always shown with a dark overlay (about 60 to 75% black) so white type sits on top
  - people appear in circular crops
- **Lists:** the site marks feature lists with a check mark ("✓ Competitive Pricing"). Use the same pattern in dashboard checklists.
- **Quotes:**
  - large Gilda Display in Silver, with curly quotes
  - the attribution sits above or below in small PT Serif ("Warren Johnson, Sales Manager at Kerrisdale Lumber")
- **Cards:** Slate background, 1px border in Steel at 30% opacity, radius 12px, no drop shadows. The site is flat throughout.

---

## 6. Voice and tone

**How Kerrisdale sounds:** practical, contractor-first, confident and quietly proud of its history. It talks about schedules, budgets, deliveries and job sites, not features.

**Phrases and ideas they use**
- "We Deliver What You Need, When You Need It."
- "Build Faster to Save More."
- "Your Project Partner" and "Become a Project Partner"
- "Stay on schedule and on budget"
- "We treat every customer like a Big Fish in a Small Pond." (Warren Johnson, Sales Manager)
- "Built on Tradition, Driven by Innovation"
- Customers describe them as family run, knowledgeable, honest, "never missed a call" and "client-first".

**Writing for the dashboard**
- Short sentences in plain trade language: quote, takeoff, PO, packing slip, yard, delivery, account.
- Frame AI the way Kerrisdale frames its own service: it removes hassle, keeps things on schedule and frees people up for the human side of the work.
- Tie it to the brand idea where it fits naturally. AI is the "driven by innovation" half of a company built on tradition.
- Respect the team's experience. Several managers have decades in the business, so don't write as if they're beginners or use hype.
- **House rules for this project:**
  - No em dashes. The website uses them, but the dashboard doesn't.
  - Canadian spelling: "labour", "colour", "organize".
  - No "unlock", "supercharge", "game-changer" or "seamless".

---

## 7. Imagery for the dashboard

- Don't use stock photos.
- If an image is needed for the hero, ask Lyle for one of the archival storefront photos or a current yard shot, and apply a 70% black overlay.
- A logo-only hero on Yard Black is the safe default until photos are supplied.
- Icons should be simple line icons (1.5px stroke) in Silver. Avoid coloured emoji.

---

## 8. Design tokens (paste into `:root`)

```css
:root {
  /* Kerrisdale palette (sampled from kerrisdalelumbercd.ca) */
  --kl-black: #000000;   /* page and header background */
  --kl-slate: #20242A;   /* cards, panels, tab bar */
  --kl-silver: #DCDCDC;  /* primary buttons, active tab, quotes */
  --kl-white: #FAFAFA;   /* headings, logo */
  --kl-ash: #B8B8B8;     /* body text */
  --kl-steel: #808080;   /* labels, dividers */

  /* Functional (dashboard only) */
  --kl-complete: #7FA383;
  --kl-progress: #C9A66B;

  /* Map to the build brief's variable names */
  --brand-primary: var(--kl-black);
  --brand-secondary: var(--kl-slate);
  --brand-accent: var(--kl-silver);
  --ink: var(--kl-white);
  --muted: var(--kl-ash);

  /* Type */
  --font-display: "Gilda Display", Georgia, serif;
  --font-body: "PT Serif", Georgia, serif;
  --font-label: "IBM Plex Mono", ui-monospace, monospace;

  /* Shape */
  --radius-pill: 999px;
  --radius-card: 12px;
}
```

---

## 9. Open items to confirm with Lyle

1. The vector logo (SVG, EPS or AI) and a black-on-transparent version
2. Whether there are official brand colours that differ from the site's monochrome look
3. Permission to use an archival storefront photo on the dashboard
4. Whether to show "Contractor Division" in the dashboard or keep "Kerrisdale Lumber" only
