# Design

Recorded from the built site (`assets/css/site.css`). Change the CSS tokens first, then update this file.

## World

Black ground, electric blue panels, an orange ember. Oversized tight headlines; the work sits on blue plates; orange marks one thing per view. Layout learned from a Behance reference the user chose: compact wordmark, Menu pill, a blue panel of numbered rows that open in place, and a gradient panel with a giant cropped wordmark.

## Colour

| Token | Dark (default) | Light | Job |
|---|---|---|---|
| `--bg` | #08080A | #F6F6FA | Page ground |
| `--bg-2` | #14141B | #ECEDF7 | Board cells, simulation panel |
| `--ink` | #F5F5F7 | #0B0B12 | Headings |
| `--ink-2` | #C8C8D0 | #3A3A48 | Body copy |
| `--muted` | #9A9AA6 | #5C5C6E | Labels, captions |
| `--line` | #24242D | #DCDDE8 | Hairlines |
| `--blue` | #2F3BFF | same | Fills: panels, pills, bars |
| `--blue-ink` | #9AA3FF | #2F3BFF | Blue as text: links |
| `--on-blue` / `--on-blue-2` | #FFFFFF / #DADDFF | same | Text on blue |
| `--orange` | #FF6A1A | same | Fills: primary button, orb, active step, lowest score |
| `--accent` | #FF6A1A | #B83A08 | Orange as small text: the marked fact, focus ring |
| `--orange-display` | #FF6A1A | #E2560E | Orange for display-size text only (3:1 rule) |

Rules: dark blue is never small text on black (use `--blue-ink`); orange never sits on blue as text. Every text pair passes 4.5:1, display text 3:1, measured on the rendered gradients.

## Gradients

- `--hot`: electric blue (#4A55FF to #161C9E) with an orange ember at 80% 82% and a faint lavender light at the top left. Hero panel, About intro (ember moved to the top right there so it never sits under text).
- `--hot-quiet`: blue with a small ember tucked into the bottom-right corner, beyond the text. Work index, screenshot plates.

## Type

Be Vietnam Pro, self-hosted (400, 600, 700). Body 18px / 1.65. Hero statement `clamp(38px, 6.2vw, 84px)`, tracking -0.055em, max 19ch. Index title `clamp(36px, 5.6vw, 72px)`. Vietnamese gets looser leading on tight display lines (`html[lang="vi"]`).

## Components

- **Header**: wordmark `hạo.` (orange dot), links on wide screens, EN/VI segmented control, theme switch (role=switch), Menu pill under 720px opening a sheet (Esc closes, focus moves in).
- **Ember panel**: process row, role line, giant cropped `Hạo`, orange orb.
- **Work index**: blue panel, rows 01 to 04 as `<details>`, plus icon that rotates into a minus, short summary and link inside.
- **Plate**: screenshot on `--hot-quiet`, 14px image radius, caption in `--on-blue-2`.
- **About board**: 12-column grid on a faint 32px grid; cells on `--bg-2`, 22px radius; section labels are blue pill `h2`s; intro cell on `--hot`; portrait cell with a blue multiply fade; objective cell solid blue with an orange underline.
- Unchanged from before: chapter rails, stats, USE scale (now blue bars, orange for the lowest), The Hook simulation, BloomMate day slider, timelines.

## Motion

Red-pen underline now orange; reveal on scroll; numbers count up; index plus rotates; theme switch knob slides. All off under reduced motion.

## Copy

All copy in `i18n/en.js` and `i18n/vi.js`. No em dashes, no clichés, no invented facts.
