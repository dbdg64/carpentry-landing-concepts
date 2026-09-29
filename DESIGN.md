---
name: ورشة حِرَف
description: Stencilled, plain-spoken, unhurried — a Cairo carpentry workshop read on a phone at night.
colors:
  iron-oxide: "#E36935"
  shed-floor: "#18110D"
  worktop: "#251C18"
  bone: "#F5F1EC"
  bone-dim: "#CFCAC2"
  pencil: "#A69D93"
  hairline: "rgba(245, 241, 236, 0.13)"
  hairline-strong: "rgba(245, 241, 236, 0.28)"
typography:
  display:
    fontFamily: "Reem Kufi, Almarai, system-ui, Segoe UI, Tahoma, sans-serif"
    fontSize: "clamp(2.125rem, 1.3rem + 3.3vw, 3.375rem)"
    fontWeight: 600
    lineHeight: 1.35
    letterSpacing: "0"
  headline:
    fontFamily: "Reem Kufi, Almarai, system-ui, Segoe UI, Tahoma, sans-serif"
    fontSize: "clamp(1.5rem, 1.15rem + 1.5vw, 2.25rem)"
    fontWeight: 600
    lineHeight: 1.4
  title:
    fontFamily: "Reem Kufi, Almarai, system-ui, Segoe UI, Tahoma, sans-serif"
    fontSize: "1.3125rem"
    fontWeight: 600
    lineHeight: 1.5
  body:
    fontFamily: "Almarai, system-ui, Segoe UI, Tahoma, Arial, sans-serif"
    fontSize: "1.0625rem"
    fontWeight: 400
    lineHeight: 1.8
  label:
    fontFamily: "Almarai, system-ui, Segoe UI, Tahoma, Arial, sans-serif"
    fontSize: "0.9375rem"
    fontWeight: 700
    lineHeight: 1.8
  micro:
    fontFamily: "Almarai, system-ui, Segoe UI, Tahoma, Arial, sans-serif"
    fontSize: "0.8125rem"
    fontWeight: 400
    lineHeight: 1.8
rounded:
  none: "0px"
  sharp: "2px"
  chip: "3px"
  panel: "4px"
  pill: "999px"
spacing:
  type-micro: "0.8125rem"
  type-label: "0.9375rem"
  type-body: "1.0625rem"
  type-title: "1.3125rem"
  gutter: "clamp(1.15rem, 4vw, 2.5rem)"
  block: "clamp(3.5rem, 8vw, 6.5rem)"
  measure: "72rem"
components:
  button-accent:
    backgroundColor: "{colors.iron-oxide}"
    textColor: "{colors.shed-floor}"
    rounded: "{rounded.chip}"
    padding: "0 1.35rem"
    height: "48px"
  button-accent-hover:
    backgroundColor: "{colors.bone}"
    textColor: "{colors.shed-floor}"
  button-outline:
    backgroundColor: "transparent"
    textColor: "{colors.bone}"
    rounded: "{rounded.chip}"
    padding: "0 1.35rem"
    height: "48px"
  button-ink:
    backgroundColor: "{colors.shed-floor}"
    textColor: "{colors.bone}"
    rounded: "{rounded.chip}"
    padding: "0 1.35rem"
    height: "48px"
  button-ink-outline:
    backgroundColor: "transparent"
    textColor: "{colors.shed-floor}"
    rounded: "{rounded.chip}"
    padding: "0 1.35rem"
    height: "48px"
  panel:
    backgroundColor: "{colors.worktop}"
    textColor: "{colors.bone-dim}"
    rounded: "{rounded.panel}"
    padding: "clamp(1.4rem, 3vw, 1.9rem)"
  job-sheet-row:
    typography: "Almarai 400 0.9375rem"
    padding: "1.1rem 0"
  placeholder-slot:
    backgroundColor: "{colors.worktop}"
    textColor: "{colors.bone}"
    rounded: "{rounded.panel}"
    padding: "1.1rem"
    height: "3 / 2 aspect"
---

# Design System: ورشة حِرَف

## 1. Overview

**Creative North Star: "The Stencilled Crate"**

A crate arrives at a workshop, gets its contents marked in paint so the right lid comes off in
the right warehouse, and never gets repainted. This system is that crate. It is a marking system
for a specific trade, not a brand surface with a craft aesthetic applied afterward. Every mark on
it exists to say what the thing is, what it's made of, or how to reach the person who made it.

It is **mechanical, plain-spoken, and unhurried**. Mechanical because the vocabulary is the
vocabulary of the trade — gauge, shim, kerf, grain — used as texture rather than as a claim about
quality. Plain-spoken because the Egyptian Arabic should sound like a workshop owner explaining his
job, not copy being written about him. Unhurried because nothing on this page pressures the reader,
which is the exact opposite of the workshop's real pressure, which is getting a door hung.

The page is dark because of a physical fact, not a mood: the reader is on a phone at 10pm in a dim
room, where a near-white page is glare. That single constraint settles the palette, the type
weight, and the reason there is exactly one accent color. It also means warmth is carried entirely
by material and language. A warm-tinted background was tried and rejected precisely because "warm"
was doing work the copy should be doing.

**Key Characteristics:**
- One ground, one accent, hairline separation. No fills between sections, no tinted bands.
- One signature pattern: the job sheet — an uneven list of uneven rows, ruled with hairlines, that
  replaces any grid of identical service cards.
- Type does the work color refuses to do. One Kufi display voice, one quiet body voice.
- Flat. There is not a single shadow in the system.
- Radius is nearly absent (2–4px). Corners are square because a crate's are.

**Explicitly rejected** (from PRODUCT.md): warm-neutral near-white body backgrounds, the repeated
uppercase kicker, grids of identical cards each with a rounded icon box, the editorial-typographic
lane, the SaaS landing template, and the MENA-startup geometric-sans look (Cairo / Tajawal).

## 2. Colors

A near-black warm ground with a single oxidised orange carrying every accent role in the system.

### Primary
- **Iron Oxide** (`#E36935` / `oklch(0.66 0.165 42)`): the only saturated color in the system. It
  marks the group headers of the job sheet, the step numerals, bullet ticks, the swap-slot labels,
  links, and the focus ring. It becomes a full drenched field exactly once, on the contact band,
  to close the page.

### Secondary (optional; omit if the project has only one accent)
- **Fired Ground** (`oklch(0.56 0.15 40)`): a *reserved* darker oxide. It exists so that
  `ink-on-accent` failure (see The Inverted Ink Rule) has a documented escape. It is currently
  used only as a hover target on `#E36935` fills, never as a standalone text color.

### Tertiary (optional)
- None. A second accent would break The One Voice Rule.

### Neutral
- **Shed Floor** (`#18110D` / `oklch(0.185 0.014 48)`): the page ground. Chosen to sit below the
  OLED-black-adjacent floor of pure #000 while retaining a trace of warm hue.
- **Worktop** (`#251C18` / `oklch(0.235 0.016 48)`): the single raised surface, used only by the
  hero scope panel and the image placeholder slots. There is no second raised tier.
- **Bone** (`#F5F1EC` / `oklch(0.96 0.008 75)`): all headings and primary UI text.
- **Bone Dim** (`#CFCAC2` / `oklch(0.84 0.012 75)`): body copy at default weight.
- **Pencil** (`#A69D93` / `oklch(0.70 0.018 70)`): supporting copy, service descriptions, hours.
  Never body copy on a Worktop surface at small sizes — see the contrast floor below.
- **Hairline** (`rgba(245,241,236,0.13)`) and **Hairline Strong** (`0.28`): translucent ink, never
  a grey. Divider lines inside lists, borders on panels, the dashed edge of a placeholder slot.

### Named Rules

**The One Voice Rule.** One saturated color, Iron Oxide, and it appears on no more than roughly
10% of any given screen. Its rarity is the entire point. The contact band is the single
sanctioned exception where the accent becomes the field, and it is permitted to do so exactly once
per page.

**The Inverted Ink Rule.** Light ink on Iron Oxide measures **2.95:1 and fails WCAG AA**. It is
prohibited, everywhere, without exception. Accent fills carry Shed Floor as their text color
(5.63:1), which is why the primary button reads as dark letters on orange paint rather than white
letters on orange. The focus ring inverts along with it: on any Iron Oxide field, the ring becomes
Shed Floor, because an Iron Oxide ring on Iron Oxide is invisible.

**The Measured Floor Rule.** Every text/background pair in this system is verified numerically
before it ships, and the lowest passing pair is 5.04:1. No pair is approved on visual impression.
A candidate that looks acceptable but measures below 4.5:1 is rejected regardless.

## 3. Typography

**Display Font:** Reem Kufi (fallback: Almarai → system-ui → Segoe UI → Tahoma → sans-serif)
**Body Font:** Almarai (fallback: system-ui → Segoe UI → Tahoma → Arial → sans-serif)
**Label/Mono Font:** none. Monospace is costume here and is forbidden — see Do's and Don'ts.

**Character:** Reem Kufi is a Kufi, the angular signage tradition used on Cairo shopfronts and
crate stencils. It is blocky, geometric, and unmistakably not a Latin display face. Paired against
Almarai, a quiet humanist Arabic sans, it produces a real contrast axis — signage against print —
rather than two similar sans pretending to be a pairing. Reem Kufi is used **only** at display
sizes (1.3125rem and up); below that it becomes a heavy, tiring texture and is not permitted.

### Hierarchy
- **Display** (600, `clamp(2.125rem, 1.3rem + 3.3vw, 3.375rem)`, 1.35): the hero headline only. One
  per page. Capped at 3.375rem, well under the 6rem ceiling, because the page is a phone document
  and a larger display size would be shouting.
- **Headline** (600, `clamp(1.5rem, 1.15rem + 1.5vw, 2.25rem)`, 1.4): section headings. These
  replace the kicker entirely — a heading is expected to identify its own section.
- **Title** (600, `1.3125rem`, 1.5): job-sheet group headers and step titles.
- **Body** (400, `1.0625rem`, 1.8): running copy. Capped at **60ch** for Arabic prose. The 1.8
  leading is deliberate — Arabic needs more vertical room than Latin at the same optical size, and
  this is a night-reading page.
- **Label** (700, `0.9375rem`): list terms, button text, navigation. Bold carries the hierarchy
  that size alone cannot.
- **Micro** (400, `0.8125rem`): the `<dt>` terms in the wood and hours lists, legal footer text,
  and the "Address is a placeholder" disclosure. Small but never lighter than Pencil on Shed Floor.

### Named Rules

**The Kufi Floor Rule.** Reem Kufi is a display face and is banned below `1.3125rem`. Body copy,
list descriptions, and hours are always Almarai. A heading that needs to shrink to fit has its copy
rewritten instead.

**The No Letterpress Rule.** `letter-spacing: 0` on every Kufi setting. Kufi is already a spaced,
stencil-like construction; adding tracking turns it into a fashion wordmark, which is precisely the
register this page must not have.

## 4. Elevation

This system uses **no shadows whatsoever** — there is not a single `box-shadow` declaration in the
stylesheet, and adding one is a regression. Depth is conveyed tonally and structurally instead:
Shed Floor for the page, Worktop for the two raised surfaces, and Hairline for every division. A
list is separated from its neighbors by a 1px translucent-ink rule, never by a floating card with a
soft edge. This is a crate: the thing is flat, and the lines are painted on.

### Shadow Vocabulary
- None. If a future component seems to need one, the correct fix is a new surface tone or a
  hairline, not an elevation.

### Named Rules

**The Flat-By-Default Rule.** Surfaces are flat at rest and stay flat in every state. The only
permitted state change is a color or border shift. There is no lift, no glow, no drop, no blur.
The one exception in the system is the focus ring, which is a 3px solid outline with a 3px offset
and is never removed for any reason.

## 5. Components

Buttons, panels, and rules. Nothing here is soft, floating, or rounded more than it needs to be.

### Buttons
- **Shape:** barely rounded (3px). A button is a cut piece of metal, not a pill. The `pill` radius
  token exists solely for the Bullet Dot and is never applied to a button.
- **Primary (`btn-accent`):** Iron Oxide fill, Shed Floor text, 48px minimum height, 1.35rem inline
  padding, 700 weight, Almarai. The WhatsApp action. The label is written as a real action
  ("Send the measurements on WhatsApp"), never "Submit" or "Learn more".
- **Hover / Focus:** background shifts to Bone with Shed Floor text — an inversion, not a darkening.
  Transitions are `0.16s cubic-bezier(0.22, 1, 0.36, 1)`, ease-out with no bounce. Focus is a 3px
  Iron Oxide outline at 3px offset, inverting to Shed Floor on any Iron Oxide field.
- **Secondary (`btn-line`):** transparent fill, Hairline Strong border, Bone text. The phone number.
  Goes to a Bone border on hover.
- **Inverted pair (`btn-ink`, `btn-ink-line`):** Shed Floor fill with Bone text, and transparent with
  a Shed Floor border. These exist **only** on the Iron Oxide contact band. Using them on a dark
  field is a bug.

### Chips
- **Style:** Iron Oxide fill, Shed Floor text, 3px radius, Micro size, 700 weight. Used for exactly
  one thing: the "placeholder image" label on an unfilled slot.
- **State:** static. There are no selectable, filterable, or toggleable chips in this system, and
  adding any would be scope invented rather than needed.

### Cards / Containers
The system has **no cards.** This is a load-bearing decision, not an omission. Service information
is presented as the **job sheet**: three columns, each headed by a title in Iron Oxide over a 2px
Iron Oxide rule, each containing a `<dl>` of hairline-separated rows with no shared container, no
background, and no border around the group. The columns hold different numbers of rows (3 / 4 / 5)
with different description lengths, so nothing repeats at a glance.

- **Corner Style:** 4px where a container is unavoidable (the hero scope panel, placeholder slots).
- **Background:** Worktop, or Shed Floor with a Hairline border. Never both.
- **Shadow Strategy:** none — see Section 4.
- **Border:** 1px Hairline. The 2px Iron Oxide rule under a job-sheet group header is the only
  thicker border in the system and it is reserved for that one role.
- **Internal Padding:** `clamp(1.4rem, 3vw, 1.9rem)` for panels.

### Inputs / Fields
None. This page collects nothing — it routes to WhatsApp and a phone call. If a contact form is
ever added it must match the outline button treatment exactly: transparent fill, Hairline Strong
border, 3px radius, Shed Floor text, 48px height, and the same Iron Oxide focus ring.

### Navigation
- **Style:** a flat Shed Floor bar with a single Hairline bottom border, sticky at the top with
  `z-index: 20`. No blur, no translucency, no shadow. Links are Almarai at label size, 500 weight,
  44px minimum height.
- **Default / hover / active:** default is Bone Dim; hover shifts to Bone with a 2px Iron Oxide
  `border-inline-start` appearing on the inline-start edge — the one place a side border is
  permitted, because it is an RTL-direction state marker rather than a decorative stripe, and it is
  2px of accent, never a thick colored rail.
- **Mobile treatment:** links collapse behind a 44×44px hamburger in the same bar. The open menu
  is a full-bleed Shed Floor panel below the bar with a Hairline Strong bottom border, 48px rows.
  The WhatsApp chip is present in the bar from 30rem up; below that the hero carries it. Escape
  closes the menu.

### The Job Sheet (signature component)
The component that replaces the service-card grid. Structure:

```
[Iron Oxide title, 2px Iron Oxide rule beneath]
<dt> term, Bone, 700 </dt>
<dd> one concrete sentence, Pencil, 0.9375rem, 40ch max </dd>
— hairline
[next row]
```

Rules: exactly one `<dt>` and one `<dd>` per row; a row is never split across columns; descriptions
name what is and is not included rather than listing benefits; no row uses an icon, a bullet, or a
card boundary. This component is why the page can present twelve services without once becoming a
template.

### The Spec Ticket (secondary signature)
A four-column hairline-separated strip under the hero, two columns on mobile, carrying only
factual parameters: workshop address, materials worked, service area, opening hours. It is the only
element on the page permitted to look like a table, because that is what it is. Values are Shed
Floor for the term in Pencil, Bone for the value.

## 6. Do's and Don'ts

### Do:
- **Do** measure every text/background pair numerically before shipping it. The floor is 4.5:1 and
  the system currently holds 5.04:1 as its worst case.
- **Do** put Iron Oxide text only on Shed Floor (5.63:1) or Worktop (5.04:1). It is not legible on
  lighter surfaces.
- **Do** carry Shed Floor as the text color on any Iron Oxide fill, and invert the focus ring with
  it.
- **Do** keep every interactive target at **44px minimum in both axes**, including the skip link and
  the hamburger.
- **Do** keep the job sheet uneven. Equal row counts across the three columns defeat the component.
- **Do** use `margin-inline`, `padding-inline`, `inset-inline-*` for anything direction-sensitive so
  the page survives an LTR toggle without repair. Verify at 320, 360, 414, 768, 1024, and 1440 —
  all currently clean with no horizontal overflow.
- **Do** keep Reem Kufi at `1.3125rem` and above. It is a stencil, not a text face.
- **Do** write commitments the workshop could actually honour on a phone call. Specific timings,
  named materials, stated limits. This is what substitutes for social proof.
- **Do** label unfilled image slots honestly and visibly, as this page does with "placeholder image"
  chips and registration marks.
- **Do** respect `prefers-reduced-motion: reduce` with a genuine alternative, not a faster version
  of the same animation. Entrance reveals must enhance an already-visible default: no class-gated
  visibility, so a paused tab or headless renderer still ships the content.

### Don't:
- **Don't** reintroduce a warm-neutral near-white body background (cream / sand / paper / bone,
  roughly OKLCH L 0.84–0.97). PRODUCT.md names this as the saturated default of 2026 brand pages,
  and it is glare at the 10pm reading this page was designed for.
- **Don't** put a small uppercase kicker above section headings. One named kicker is voice; a kicker
  on every section is scaffolding, and it was removed from this page for exactly that reason.
- **Don't** build a grid of identical cards, and never a rounded icon box above a heading. Six of
  those reads as a template, not as six services. The job sheet exists to prevent this.
- **Don't** add a `box-shadow`. The system is flat. See Section 4.
- **Don't** use `backdrop-filter`, `blur()`, or any translucent floating surface. That is
  glassmorphism and it is prohibited.
- **Don't** use a gradient as a background or as text. None exist in this system and none should.
- **Don't** use a `border-left` / `border-right` thicker than 1px as a colored stripe on any card,
  row, or callout. The single exception is the 2px `border-inline-start` on a hovered nav link,
  which marks state direction rather than decorating a container.
- **Don't** pair a second humanist sans with Almarai, and don't reintroduce IBM Plex Sans Arabic or
  Readex Pro here — the earlier pairing was too similar to do any work. Neither is a prohibited
  font, but the pairing was rejected on effect.
- **Don't** set light ink on Iron Oxide. 2.95:1. This is the single most likely way to break the
  color system, because the instinct to put white on a saturated fill is strong.
- **Don't** use monospace as shorthand for "technical" or "craft." The brand is not a developer
  tool; mono reads as costume here.
- **Don't** invent social proof — no fabricated counts, testimonials, or named customers. A craft
  buyer detects this and it costs more trust than it buys.
- **Don't** use em-dashes as a cadence tic. The copy carries one, down from eight in the first
  draft. Use a period, a comma, or a colon.
- **Don't** apply `text-wrap: balance` to running prose. It is for headings only; on paragraphs it
  produces visibly uneven last lines.
