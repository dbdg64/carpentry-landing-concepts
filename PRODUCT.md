# Product

## Register

brand

## Users

The primary reader is a Cairo resident, **on a phone, at home in the evening**, with the
workshop's WhatsApp thread open in another tab. They are not browsing — they are
shortlisting two or three workshops and trying to decide which one will not disappear
mid-job. They arrived from a search or a neighbour's recommendation, not from a brand
ad, so they have no prior vocabulary for the trade and are reading for signals of
reliability rather than for style.

Secondary reader: **you**, reviewing this as a portfolio piece. You are checking whether
the design decisions are defensible and specific, not whether it decorates well. An
audience of one, but the more demanding one.

The scene is the constraint that matters: a near-white page at 10pm on a phone in a dim
living room is not neutral, it is glare. Evening use is a physical argument for a dark
ground, not a stylistic preference.

## Product Purpose

A single-page landing page for a fictional Cairo carpentry workshop, built as portfolio
concept work. Its real job is to move a qualified reader into a WhatsApp conversation
with a measurement in hand. Success is the reader sending a real message; the page is a
funnel, not a brochure.

As portfolio work, the second success condition is that every visible decision traces
back to a stated reason. A choice that cannot be justified is a liability here.

## Brand Personality

**mechanical · plain-spoken · unhurried**

- *mechanical* — the vocabulary of the trade: gauge, shim, kerf, grain, dado. Precision
  as texture, not as a claim about quality.
- *plain-spoken* — Egyptian Arabic that sounds spoken, not translated. The page should
  read like the workshop owner explaining his job, not like a copywriter describing it.
- *unhurried* — no countdown timers, no "act now", no manufactured urgency. The opposite
  of the workshop's real pressure, which is getting a door hung.

Physical reference points: an iron-oxide stain tin, oxidised brass on a hand plane,
sawdust on dark concrete, stencilled crate markings on a shopfront. Warmth in this brand
is carried by material and copy — **not** by a warm-tinted page background.

## Anti-references

Specific to this page. The first three are things the current build does wrong and must
stop doing:

- **A warm-neutral near-white body background** (cream / sand / paper / bone, roughly
  OKLCH L 0.84–0.97). This is the saturated default of 2026 brand pages. A dark ground is
  both the register-correct answer and the physically correct one for a 10pm phone.
- **A small uppercase kicker repeated above every section heading.** One named kicker is
  voice; a kicker on every section is scaffolding.
- **A repeated grid of identical cards, each with a rounded icon box above a heading.**
  Six of them reads as a template, not as six services.
- The editorial-typographic lane (display serif + italic + rule-separated columns).
- The SaaS landing template in general: sticky translucent nav, hero + three feature
  cards + logo strip + CTA band.
- The MENA-startup geometric-sans look (Cairo / Tajawal, the default Arabic web pairing).
  It signals a real-estate app, not a workshop.
- Fabricated social proof of any kind: invented counts, invented testimonials, invented
  named customers. A craft buyer can smell this and it costs more trust than it buys.

## Design Principles

1. **Every claim must survive a phone call.** Anything stated on the page should be
   something the workshop could actually honour — specific timings, named materials,
   stated limits. This is what rules out fake stats, and it is also the actual
   differentiator against every other workshop site.
2. **Design for the 10pm sofa, not the showroom.** Decisions get made at night on a
   phone. Treat light-mode as a decision requiring justification, never as the default.
3. **The reader is comparing three tabs.** Differentiate on specifics a competitor would
   not bother to state — what is excluded, how long, what the wood does over time — not
   on adjectives that any competitor can also claim.
4. **A labelled placeholder beats a fake photograph.** Reserve image slots with honest
   labels and a swap list. Invented imagery destroys the credibility the copy works to
   build.
5. **Earn the accent, then stop.** Colour is a commitment axis, not decoration. A single
   committed colour; the restraint around it is what makes it land.

## Accessibility & Inclusion

- **WCAG 2.2 AA is the floor**, verified numerically rather than by eye. All text pairs
  must be measured in the palette actually shipped, not estimated.
- **Arabic RTL is the primary authoring direction**, not a mirrored afterthought. CSS
  logical properties throughout (`margin-inline`, `padding-inline`, `inset-inline-*`).
  Reflow must survive an LTR toggle without layout repair.
- **Reduced motion is mandatory.** Every animation needs a `prefers-reduced-motion`
  alternative. Entrance reveals must enhance an already-visible default, never gate
  content visibility behind a class-triggered transition.
- **Two colour rules established by measurement, not taste:**
  - Light ink on the terracotta accent measures **2.95:1 and fails**. Accent fills must
    carry the dark ground colour as their text (5.63:1). This is a hard rule, not a
    preference.
  - Accent used as *text* is only permitted on `ground` (5.63:1) and `surface-1`
    (5.04:1). It is not permitted on lighter raised surfaces.
- Tap targets **≥ 44px** in both axes, on a phone-first layout.
- Do not encode meaning in colour alone; pair any status colour with a label or icon.
