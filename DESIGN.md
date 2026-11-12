# Design system

Portfolio of Shakkeer Thottathil, software consultant and developer for
small and mid-sized businesses. The site's job is to get a business owner
to send an email.

## Direction

Shop paperwork turned into software. The page is a cool, quiet sheet of
paper with navy ink; the only colourful things are the handwritten papers
on the 3D desk, which flip into app screens. Everything outside the desk
stays plain so the desk is the one memorable element.

Feeling: practical, calm, approachable. Written for a shop owner, not for
another developer. No code motifs, no terminal styling, no gradients.

This direction comes from the brief and the existing page. It was not
compared against other real websites.

## Colour

All colours are CSS variables in `:root` of `index.html`.

| Token | Light | Dark | Role |
|---|---|---|---|
| `--paper` | `#F6F7F9` | `#12152A` | Page background; text on primary buttons |
| `--ink` | `#1C2140` | `#E6E8F2` | Headings and main text |
| `--muted` | `#565C76` | `#A3A8C2` | Secondary text, captions, footer |
| `--carbon` | `#3446B0` | `#9AA8FF` | Primary: buttons, links, step numbers |
| `--carbon-hover` | `#26358C` | `#BAC3FF` | Hover state of primary |
| `--rule` | `#D5D9E4` | `#2C3150` | Section dividers only |
| `--focus` | `#3446B0` | `#BAC3FF` | Keyboard focus ring |
| `--mat` / `--mat-edge` | `#232A5C` / `#171C44` | `#2B3370` / `#1C2250` | Desk surface and its sides |
| `--slip`, `--slip-line`, `--slip-ink` | `#F7EDB4`, `#E3D58C`, `#2A3A9E` | same | Yellow order slip, its ruled lines, handwriting ink |
| `--success` | `#1D7A4E` | same | "Done" status inside app screens |
| `--warning` / `--warning-fill` | `#A1440B` / `#D9641A` | same | Low-stock text / bar inside app screens |
| `--screen-*` | white card, ink, muted, primary, border, rule | same | App screens on the back of each paper; light in both themes |

Rules:

- One primary colour (carbon blue). No second accent on the page itself.
- The paper colours (yellow, pink, pale blue, off-white) belong to the
  desk illustration only. Never use them for page UI.
- Measured contrast: ink on paper 14.6:1, muted 6.1:1, carbon 7.4:1;
  dark theme 14.7, 7.7 and 8.1. Success and warning on white 5.3 and 6.3.

## Typography

| Token | Value | Role |
|---|---|---|
| `--font-sans` | Schibsted Grotesk 400 / 500 / 700 | All page text |
| `--font-hand` | Kalam 400 | Handwriting on the desk papers only |
| `--text-display` | `clamp(1.75rem, 6.2vw, 4.5rem)`, line 1.05 | The email address |
| `--text-h1` | `clamp(2.25rem, 4.3vw, 3.5rem)`, line 1.04 | Page headline |
| `--text-h2` | `clamp(1.6rem, 3vw, 2.125rem)`, line 1.15 | Section headings |
| `--text-lg` | 1.25rem | Lede paragraphs, h3 |
| `--text-base` | 1.125rem, line 1.55 | Body |
| `--text-sm` | 1rem | Navigation, buttons, captions, step text |
| `--text-xs` | 0.9375rem | Footer |

Rules: sentence case everywhere; no all-caps labels; headings are weight
700 with slightly negative tracking; body lines stay under `--measure`
(36rem, about 65 characters). Text inside the desk papers and screens is
sized in px because it is artwork that scales with the scene.

## Spacing and layout

4px-based scale: `--space-3` 0.75rem, `--space-4` 1rem, `--space-5`
1.25rem, `--space-6` 1.5rem, `--space-8` 2rem, `--space-10` 2.5rem,
`--space-12` 3rem.

- `--section`: `clamp(3rem, 7vw, 5.5rem)` above and below each section.
- `--content`: 72rem maximum width; side gutter `--space-6`, `--space-4`
  under 480px.
- Everything is left aligned. Nothing is centred.
- Sections are separated by a single 1px `--rule` line, not by boxes.

## Shape and depth

| Token | Value | Role |
|---|---|---|
| `--radius-pill` | 999px | Buttons |
| `--radius-sm` | 4px | Focus ring, desk corners |
| `--radius-paper` | 3px | Papers on the desk |
| `--radius-screen` | 10px | App screens |

No shadows on page UI. The only shadows are the ones the papers cast on
the desk, because they show height.

## Components

- **Primary button**: carbon fill, paper text, pill, weight 500. Hover:
  `--carbon-hover`. Says exactly what it does ("Email me about your
  project").
- **Secondary button**: same shape, no fill, 1.5px carbon outline.
- **Quiet action**: plain underlined link in carbon ("Put it back").
- **Links**: carbon, 1px underline. Navigation links are ink with the
  underline appearing on hover.
- **Focus**: 3px `--focus` outline, 3px offset, on every interactive
  element; yellow `--focus-on-dark` on the desk papers.
- **Service block**: h3 plus one short paragraph, no card, no icon.
- **Process step**: 2px ink top rule, step number in carbon, h3, one
  paragraph. Numbered because the steps happen in order.
- **Desk scene**: papers lift on hover, and on click turn to face the
  visitor and flip to an app screen. One paper open at a time. Motion
  only answers the visitor; nothing animates on its own. Reduced-motion
  setting removes the transitions.
- **Footer**: one line of muted text.

There are no form inputs or cards yet. If a contact form is added, inputs
use a 1.5px `--rule` border, `--radius-sm`, and the focus ring above.

## Imagery and icons

- No icon set and no emoji. Labels are words.
- The desk is the only illustration. New examples of work should be added
  as another paper on the desk or as real screenshots, not stock images.
- Project screenshots, when added, sit flat with a 1px `--rule` border
  and no shadow.
