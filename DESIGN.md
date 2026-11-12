# Design

Recorded from the built site (`assets/css/site.css`), not from intentions. Change the CSS tokens first, then update this file.

## World

Apple-like quiet: a near-white ground, ink type, one red-pen accent. Product screenshots carry all other colour. Pages read slowly: large statements, wide margins, one idea per screen.

## Colour

| Token | Light | Dark | Job |
|---|---|---|---|
| `--bg` | #FBFBFD | #111113 | Page ground |
| `--bg-2` | #F2F2F5 | #1B1B1E | Simulation panel, segmented control, image wells |
| `--ink` | #1D1D1F | #F5F5F7 | Headings, primary button |
| `--ink-2` | #424245 | #D2D2D7 | Body copy |
| `--muted` | #5E5E64 | #A6A6AC | Labels, captions, inactive steps |
| `--line` | #E1E1E6 | #2E2E33 | Hairlines, image borders, tracks |
| `--accent` | #C2402A | #FF7A5C | The marked fact, links, focus ring, active step, the lowest score |

Dark mode follows the system only. Accent text passes 5:1 on the ground in both themes. Accent is never a fill for large areas.

## Type

Be Vietnam Pro, self-hosted (400, 600, 700; Latin, Latin Extended, Vietnamese). Body 18px / 1.65. Lead `clamp(19px, 1.6vw, 22px)`. Statements (`.say`, `.big`) `clamp(32px, 4.6vw, 57.6px)`, weight 600, tracking -0.032em, max 22ch. Display (name, case study titles, Contact) `clamp(48px, 9vw, 96px)`, weight 700, tracking -0.04em. Numbers use tabular figures.

## Layout

Content width 75rem with 20px gutters (16px under 420px). Reading column 42rem. Sections separated by hairlines and 72 to 170px of space; no cards around text. Global nav scrolls away; a translucent local rail (chapter name and Observe/Decide/Test on the home page, section contents on case studies) sticks to the top.

## Components

- **Screenshot** (`.shot`): 14px radius, 1px hairline, soft offset shadow, caption below in muted small text.
- **Placeholder** (`.ph`): dashed hairline well naming the exact file it waits for.
- **Stat** (`.stat`): hairline on top, large tabular number, small unit, muted label.
- **Lists** (`.decisions`, `.criteria`, `.timeline`, `.flow`): hairline rows; numbers only where order matters.
- **Buttons**: pill. Ink-filled primary, hairline secondary. Text links in accent with an arrow that moves 3px on hover.
- **Simulation** (`.sim`): the one framed object (24px radius on `--bg-2`), because it is a working kiosk. Choices tilt ±1.6° toward their side, like the head tilt they stand for.
- **Day slider** (`.day`): native range input with an accent progress fill and four tappable stops; panels cross-fade.
- **USE scale** (`.scale`): bars drawn to scale from 1 to 7; the lowest score in accent.

## Motion

One authored moment: the red-pen underline draws once under each observed fact. Content below the fold fades up 24px once; numbers count up once. Ease `cubic-bezier(0.16, 1, 0.3, 1)`. Everything is visible at rest and without JavaScript. Reduced motion removes all movement; the simulation and slider still work. Reduced transparency makes the rail solid.

## Copy

All copy lives in `i18n/en.js` and `i18n/vi.js`. No em dashes, no clichés. Illustrative content, sample data and plans are labelled as such. Missing facts are `[TODO: ...]`, never guessed.
