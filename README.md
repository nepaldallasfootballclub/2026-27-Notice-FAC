# NDFC Dashain Tihar Cup — Simple Notice Flyer

A short, text-first **notice** for Nepal Dallas FC, sized 1080 × 1350 (4:5
portrait — not a full 9:16 story) for Instagram, WhatsApp, or print.

It is deliberately minimal: club logo and name, a small "Club Notice" label,
the flyer title, one short paragraph, and the standard footer. No cards, price
panels, chips, icons, or banners — just the same faint pitch-line texture, soft
red/navy background wash, faint crest watermark, and torn corner accents used
across the club's other flyers.

---

## The notice

> **NDFC Dashain Tihar Cup**
>
> We would like to take a moment to thank all our **Gold Members**. Your entry
> is **FREE** for the NDFC Dashain Tihar Cup. With that said, the Cup is open to
> **EVERYONE**. Non members pay **$40**, and that **$40** can go toward a **Gold
> Membership**. Register and let's play, have fun, and make it count.

That paragraph runs five lines on the flyer, in a formal notice voice with no
hyphens or dashes. Body text is navy `#0A1740`; the highlighted words are red
`#C8102E` — `FREE`, `EVERYONE`, both `$40` amounts, and the Gold Member
references. Fonts are the club's usual set: **Anton** (title), **Manrope**
(body), **Space Grotesk** (small labels).

---

## Files

| File | What it is |
| --- | --- |
| `2026-27 NDFC Cup Notice Flyer.html` | The editable notice. Open in any browser. |
| `NDFC-Cup-Open-Invite.png` | Ready-to-post 1080 × 1350 export. |
| `NDFC_Official_Logo.png` | Original logo with its white background (backup). |
| `NDFC_Logo_Transparent.png` | Logo with the white background removed — this is what the flyer embeds, so it blends with the page and works as the watermark. |

---

## Export a PNG

1. Double-click `2026-27 NDFC Cup Notice Flyer.html` to open it in Chrome or Edge.
2. Click **Create PNG** in the top-right corner.
3. It downloads as `NDFC-Cup-Open-Invite.png`.

The fonts and PNG-export library load from the internet, so stay online while
exporting. The logo is embedded in the HTML, so local image permissions will not
break the export.

---

## Editing

Open the HTML in a text editor. The notice is plain text in the page body.

- **The paragraph** — the single `<p class="notice-text">` element. Wrap any
  word in `<span class="red">…</span>` to make it red. Keep it short; four or
  five lines is the goal.
- **Small label** — search for `Club Notice`. The short red rules on each side
  are drawn by `.kicker::before` / `.kicker::after` in the CSS (44 × 3 px each),
  matching the Birthday Wishes eyebrow treatment.
- **Title** — search for `NDFC Dashain Tihar Cup` (the `.title` element).
- **Watermark** — the `<img class="watermark">` element. Size is set by
  `width:640px` and visibility by `opacity:.05` in the CSS.
- **Footer** — search for `Play Together`.

**Logo:** the header and watermark always use the embedded transparent-background
logo (`const LOGO = "data:image/png;base64,..."` near the bottom of the file).
Any logo previously saved in the browser is cleared on load, so a
white-background version cannot reappear. To change the logo permanently, replace
that data URI with your own PNG that has a transparent background.

### Policy note

The line saying the **$40 can go toward a Gold Membership** is based on your
brief. If the club decides the $40 is a plain non-member fee, edit that sentence
before posting.

---

## Layout

- 1080 × 1350 fixed canvas (4:5), so the exported PNG matches the browser
  preview and the notice does not sit as low as on a 9:16 story.
- White background with a faint diagonal pitch-line texture and soft red/navy
  radial washes.
- Faint torn corner accents in the four corners, adapted from the countdown
  flyer (navy `#12169C` and red `#C8102E`, 11–12% opacity, behind the content).
- Centered crest watermark at 5% opacity.
- Header (logo, club name) → centered notice block (label flanked by short red
  rules, title, red rule, one paragraph) → footer (2px gold divider, tagline,
  handle).
- The notice block is vertically centered between header and footer, with a
  slight upward bias.
