# Design — Magyar Widget site

World: **Evening study.** The site borrows the app's own calm, dark prestige: a near-black study surface lit by a soft forest-green glow, cream paper for reading and for the widget itself, and a literary serif for Hungarian words. It should feel like a well-made dictionary on a night desk, not a SaaS landing page.

## Modes
- `index.html` — Persuade. Leads with the two differentiators, in this order of proof: (1) the Home Screen widget, a word in view every unlock; (2) spaced recall, words return right before you would forget them. Core decks are supporting evidence, not a headline.
- `privacy.html`, `support.html` — Read. Dark masthead frame, calm cream reading column (≤68ch), sticky "On this page" contents on desktop.

## Palette
| Token | Hex | Use |
|---|---|---|
| night | #0c0e0d | page ground, header, footer, hero |
| night-2 / night-3 | #141816 / #1c221f | recall band, hover pills |
| line-dark | #2a322e | rules on dark |
| forest | #1b4d3e | privacy band, deck bars, focus on light |
| forest-2 / forest-3 | #2f5e48 / #3f7a5e | app "Seen/Remembered" green, deck bars |
| sage | #9fc4ae | accent on dark (italic emphasis, curve, focus ring, selection) |
| cream / paper | #f6f2e7 / #fbf8f0 | light sections, reading ground, primary button |
| ink / ink-2 | #16201b / #44534a | text on light |
| on-dark / on-dark-2 | #ece8dc / #a9b6ae | text on dark |

Selection and focus rings are themed per ground (sage on dark, forest on light). Scrollbar tinted forest/night.

## Type
- Display + Hungarian words: **Newsreader** (variable, opsz, roman + italic), self-hosted woff2 in `assets/fonts/` incl. latin-ext for ő/ű. Weight 400–500, tracking −0.02 to −0.035em. Italic sage used once for emphasis ("sticks").
- UI + body: **Hanken Grotesk** (variable), self-hosted. Body 17px, 1.6.

## Signature moves
- Real device frames (CSS bezel) around real captures; hero phone bleeds off the bottom edge into the next band.
- Dictionary-entry annotation beside the hero phone (`hét · noun · week`), desktop only.
- Authored SVG forgetting-curve diagram for spaced recall (marked illustrative).
- Nested widening bars for Core 100 ⊂ 300 ⊂ 600 (decks are prefixes of one list).
- Ruled lists (hairline dividers) instead of card grids; icons are one authored SVG set, 1.75 stroke.

## Motion
One moment: hero device rises with blur-to-sharp, 1.1s exponential ease-out. Disabled under `prefers-reduced-motion`.

## Rules
No eyebrow/kicker labels, no gradient text, no nested cards, no emoji icons, no fake App Store badge, no word counts other than Core 100/300/600, no third-party publisher names. `app-home.png` is not used (it shows an error state).
