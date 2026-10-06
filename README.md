# Kerrisdale Lumber AI Accelerator Dashboard

A 30-day AI training dashboard for the Kerrisdale Lumber leadership team, built by Junction Consulting.

## What This Is

A single-page static dashboard that tracks progress through a four-session AI training program. It includes:

- **Overview** of the program, participants and success measures
- **Session pages** with agendas, homework and (after each session) summaries
- **Roadmap** for what comes after the program
- **Prompt Library** with ready-to-use prompts for collections, sales and leadership

## How to Update After Each Session

### Mark a Session Complete

1. Open `index.html` in a text editor
2. Find the session's tab button (search for `id="tab-s1"` for Session 1)
3. Change the class from `is-upcoming` to `is-complete`
4. Add the checkmark SVG to the tab eyebrow (copy from another completed tab)
5. In the session's panel, uncomment the "completed" content block and fill in:
   - Session summary
   - Key lessons
   - What we built
   - Homework for the next session
6. Update the progress bar (search for `PROGRESS-COUNT` and `PROGRESS-BAR`)
7. Update the "Next up" line (search for `NEXT-UP`)
8. Update the footer date (search for `LAST-UPDATED`)

### Update the Results Table

Search for `<!-- RESULTS -->` comments in the Overview panel. Update the "Latest" column with actual measurements.

### Add a Prompt to the Library

1. Find the template comment in the Prompt Library panel (search for `TEMPLATE: copy this card`)
2. Copy the template and paste it as the last card in the `.prompt-list`
3. Fill in: department, task title, description, the prompt text and notes
4. Set the `data-dept` attribute to one of: `collections`, `sales`, `quotes`, `ap`, `leadership`
5. Set `data-search` with lowercase keywords for search
6. Give the `<pre class="pc-prompt">` a unique id and match it on the Copy button's `data-target`

## How to Turn on GitHub Pages

1. Go to the repository Settings
2. Click Pages in the sidebar
3. Under "Source", select Deploy from a branch
4. Choose `main` branch and `/ (root)` folder
5. Click Save
6. Wait a minute, then visit `https://[username].github.io/kerrisdale-ai-training/`

## Privacy

This dashboard is designed to be publicly accessible via GitHub Pages, but it does not index in search engines (`noindex, nofollow` is set).

**Do not add to this page:**
- Customer names or account details
- Revenue, account balances or financial data
- Staff surnames (except Lyle Perry)
- Any SAP exports or real AR data

All sensitive materials should be sent directly to Junction, not uploaded here.

**Want more privacy?** You can:
- Make the repository private (requires GitHub Pro or Team)
- Add password protection using a service like Cloudflare Access

## Files

| File | Purpose |
|------|---------|
| `index.html` | The dashboard (edit this to update content) |
| `BRAND-GUIDE.md` | Brand standards reference (do not modify) |
| `kerrisdale lumber logo.png` | Logo file (do not modify) |
| `README.md` | This file |

## Technical Notes

- Single self-contained HTML file, no build step, no dependencies
- Logo is base64-embedded in the HTML
- Fonts load from Google Fonts
- Works on any modern browser, including mobile Safari
- Accessible: keyboard navigation, screen reader support, respects reduced motion preference

---

Built by [Junction Consulting](https://wearejunction.com)
