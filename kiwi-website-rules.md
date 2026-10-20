# Kiwi website: rules and guardrails

The rules every stage of the Kiwi website follows, from tokens to launch. Written in 2026 from the reference kit, the brand guidelines, the plan and the decisions made while building the kit. Claude reads this file before any Kiwi website work, alongside the reference kit page.

## 0. How to use this file

- **Order of authority.** Brand guidelines, then this file, then the reference kit page, then general good practice. If two of them disagree, stop and ask Toby. Never pick one quietly.
- **Read before every stage.** Claude Design, Claude Code and Cowork sessions load this file, the kit page and the tokens before generating anything.
- **Rules are pass or fail.** Every section is checked against the checklists in section 13 before it goes to Toby.
- **Gaps get flagged, not filled.** If a rule doesn't cover a case, say so and propose a rule. Add it here once Toby agrees.
- **Status.** Sections 4 to 9 come from the kit and decisions already made. The performance targets, the 12px minimum, line length, image sizes, pause controls and the code rules are proposed standards, pending Toby's approval.

## 1. Open items to settle before stage 4

These block or shape the design. Each needs an owner's answer.

| Item | Why it matters | Owner |
| --- | --- | --- |
| Accent shortlist: 5 palettes in the kit, the plan says 3 | The concept site and Kiwi's choice depend on it | Toby |
| Graphite Cyan reads green, Crimson Forge is a red | The plan says "don't use green, or a red that reads as danger". Either drop them or update the plan | Toby |
| Crimson shown as #ED3E33, not Figma's #EC362B | Figma's red is 4.34:1 with Kiwi black, under AA for small text. The kit lightens it 4% | Toby |
| Figma hex labels: Steel Beacon says 00A3FF (swatch #5AA9FF), Crimson says FF2D2D (swatch #EC362B) | The kit uses the swatches. Fix the labels so nobody copies the wrong value | Toby |
| Figma palettes pair each accent with a different heading and body font | The kit keeps Familjen Grotesk and Inter for every accent. Confirm fonts don't change with the accent | Toby |
| Accent icons on the website | Guidelines v1.9 now allow the accent for icons on the website. Kiwi to confirm with the guidelines sign-off | Rich and Lee |
| Key message "We design, manage and build in-house" | Changed from "manufacture" in guidelines v1.9 to match Design, Manage, Build. "In-house manufacturing" stays as a strength. Kiwi to confirm | Rich and Lee |
| "Since 1986" and "40 years" | 1986 is still to confirm with Kiwi. Every "40 years" counter rests on it | Rich and Lee |
| "3 sectors", "1 team, start to finish" | Used in the counters. Confirm they're claims Kiwi will stand behind | Rich and Lee |
| Project names: "Flight Club, Newark", "JD, Leicester Square", "Restaurant" | Taken from B2PM's site. Confirm names, and name the restaurant project or drop it | Rich and Lee |
| Client logos (JD, JD Gyms, Under Armour, Hoka, Ugg, Deckers Brands, Berghaus, Pentland Brands, Lane7, Marston's) | Permission to show them is not confirmed | Rich and Lee |
| Original project photos | The kit uses web copies from B2PM's site. The live site needs originals at full resolution | Rich and Lee |
| WordPress approach and staging | Block theme with ACF blocks recommended. Carl to confirm | Carl |

## 2. Process guardrails

- **One source of truth.** Tokens, components and copy live in the private repo. Nothing exists only in a chat, a Claude Design session or a local file.
- **Tokens before pages.** No colour, size, spacing, radius, easing or duration is typed into a component. Everything is a token.
- **Sections as blocks.** Every section is self-contained and maps one-to-one to a WordPress block or pattern. No section depends on the one above or below it.
- **Targeted edits only.** Once a section is approved, change it with small edits. Never regenerate an approved section. Commit every approved round and log it in the changelog.
- **Real content from the start.** Copy from the agreed copy deck. Gaps are marked [TBC] in the design, never filled with invented text.
- **Desktop and mobile every round.** A section isn't reviewed until it's been seen at 1440px and 390px.
- **Gates are fixed.** Toby signs off each stage. Kiwi sign off messages, accent, copy and claims. No stage starts while the previous gate is open, unless Toby says so.
- **Decisions are logged.** Any choice made during a stage goes in the decision log with who made it and when.

## 3. Content and evidence

- **Only supplied or approved claims.** No invented figures, dates, client names, quotes, testimonials or results. If a number isn't in a source, mark it [TBC] and list it.
- **Every claim traces to a source.** The copy deck records the source for each figure, date, client name and project name.
- **Unconfirmed items stay marked.** Anything in section 1 still open is shown as [TBC] or labelled "to confirm" on staging.
- **Client logos and names** go live only with Kiwi's confirmation that they can be shown.
- **Photos.** Real Kiwi projects only, credited to the right project and location. AI images only as clearly labelled placeholders in the concept, never on the live site.
- **No competitor names**, and no other agency's or consultancy's work presented as Kiwi's.

### Words

- Write **Kiwi** in copy, never "KIWI". The logo is the only place the name appears in capitals.
- Write **fit-out**, never "shopfitting".
- The strapline is **Design, Manage, Build**. Never "Design, Manufacture, Build".
- The web address is **wearekiwi.co.uk**.
- UK English. Dates written as 2 September 2026.
- Sentence case for headings, navigation and buttons ("Our work", "Learn more"). Capitals only for short labels and eyebrows.
- No em dashes in copy.
- Follow the writing style in the brand guidelines: "we" and "you", active voice, numerals (3 sites, 40 years), fit-out as a noun and fit out as a verb, no exclamation marks, "and" not "&" in sentences.
- Words to avoid (brand guidelines): solutions, turnkey, world-class, best-in-class, cutting-edge, seamless, synergy, leverage, passionate about.

### Voice

- Lead with the outcome for the client, not Kiwi's output.
- Specific over adjectival. "One team from the first drawing to handover", not "a seamless end-to-end service".
- Short sentences. One idea per sentence.

## 4. Colour

### Mono tones (fixed in every accent)

| Token | Hex | Use |
| --- | --- | --- |
| `--k` Kiwi black | #16181B | Text on white, dark backgrounds |
| `--k80` | #454649 | Rules and dividers on dark, secondary text on white |
| `--k70` | #5C5D5F | Secondary text on white |
| `--k60` | #737476 | Captions and labels on white |
| `--k40` | #A2A3A4 | Grid lines in demos, labels on dark |
| `--k10` | #E8E8E8 | Rules and dividers on white |
| `--k5` | #F3F3F4 | Surfaces on white |
| `--w` | #FFFFFF | Text on dark, page background |

### Accents (one per palette)

| Palette | `--acc` | `--acc-ink` (4.5:1 on white) | `--acc-ink3` (3:1 on white) |
| --- | --- | --- | --- |
| Site Yellow | #FFDD00 | #877500 | #AA9300 |
| Steel Beacon | #5AA9FF | #4479B4 | #5298E4 |
| Crimson Forge | #ED3E33 | #DF342A | #ED3E33 |
| Ink & Tangerine | #FF6A2C | #C25528 | #F6672B |
| Graphite Cyan | #1FC9A0 | #1B846C | #1DA787 |

- Site Yellow (#FFDD00) replaced Forge Amber as the working accent on 20 October 2026 (Toby).
- The accent is switched with one attribute on the page root (`data-accent`). Components only ever reference `--acc`, `--acc-ink` and `--acc-ink3`. Never a hex.
- **Small doses.** Highlights, eyebrow bars, the accent button, accent icons, indicator lines and counters. Never a large background area, never body text.
- **Allowed pairings:**
  - Kiwi black text on the accent (4.5:1 or better in all five).
  - The accent as text, numbers or icons on Kiwi black (4.5:1 or better in all five).
  - The accent as a fill, bar or line on white, when it's decoration or backed by another cue.
- **Not allowed:**
  - White text on the accent (fails in all five).
  - The accent as text or as the only state cue on white. Use `--acc-ink` for small text and icons, `--acc-ink3` for large text (24px, or 18.66px at weight 600 and above).
  - The accent on `--k80` for anything that must be read.
  - Two accents on one page.
- **Photography is not the accent.** Colours inside photos (the JD yellow in the hero) stay as photographed and are never matched to the accent.

## 5. Type

- **Display:** Familjen Grotesk SemiBold (600) for headings, titles and numbers. Regular (400) for subheads.
- **Body:** Inter Light (300) for body text, SemiBold (600) for emphasis and labels. The kit also uses Inter Regular (400) for navigation and buttons; confirm this in the guidelines.
- **Type scale (brand guidelines, screen):** H1 48px / 1.1, H2 28px / 1.2, H3 22px / 1.25, H4 18px / 1.3, subhead 17px / 1.45, body 16px / 1.6, label 12px capitals / 1.4 with +12% tracking. Reduce headings by about a quarter on mobile. Display type in compositions (heroes, text treatments) can go larger.
- Left-aligned. Never justify or centre long text. Arial is the fallback where brand fonts aren't available.
- Components use the tokens only.
- **Eyebrows and labels:** capitals, 11 to 16px, letter-spacing about 0.02 to 0.12em.
- **Line length:** 45 to 75 characters for body copy.
- **No text below 12px** on the live site, except legal small print.
- **Numbers** use tabular figures where they change (counters).

## 6. Grid

- **Module:** 144 × 140px at 1440 × 840, a 10 × 6 grid. Custom grids are built from the same module.
- **Lines:** 1px. Solid for cells. Dashed (6px dash, 5px gap) for diagonals and guides. Kiwi black or white, plus the grey (`--k40`) used in the grid demos.
- **Strengths:** feature 1, structure 0.35, ambient 0.15. One strength per view.
- **Sparingly.** Where it adds structure: a hero, a feature, a project grid. Most layouts stay clean.
- **Diagonals and grid lines** share one colour and weight in any one view.
- **On mobile** the grid becomes a 40px module and stays at ambient or structure strength.

## 7. Layout and components

Each component follows its reference kit figure. These are the rules that keep it right.

- **Corners.** Square everywhere. No radius on anything.
- **Hero.** A full-bleed mono photo with colour windows, the grid fading towards the copy, one eyebrow, one headline, one sentence, one button. A small counter is allowed beside the button. A dark gradient always sits behind the copy, strong enough to stay readable when the colour windows light up.
- **Hero on mobile.** Fills the screen height. The grid drops to the 40px module. The counter stacks above the button. Burger menu top right.
- **Navigation.** Desktop: links plus the Contact button. No link is underlined until it's hovered or is the current section. Mobile: burger menu.
- **Menus.** Numbered links, with the project photo on the right on hover (desktop only).
- **Text and image.** Half photo in colour, half copy, with the ambient grid on the copy side.
- **Project grid.** Project photos in colour, a location label on each. Bento on mobile, vertical scroll, no tall thin crops.
- **Cards.** The title takes the eyebrow bar on hover. The whole card is one link, with one arrow box.
- **Buttons.** Light, dark and accent. Square, 1px border, label and arrow box. On hover and focus the box fills and the arrow turns. Sentence case labels.
- **Lists and list rows.** Number, title, label, arrow box. Kiwi black fills from the left on hover.
- **Text treatments.** One lead move per layout, with at most one supporting move. Marker for a figure or date. Block for key words.
- **Eyebrows.** The eyebrow bar on white. On black or photography, the eyebrow dash or the square dot. Never the bar on dark (the bar's text can't be read there).
- **Counters.** The number counts up and takes the accent block when it lands. The label sits outside the block. No box around the counter at rest, so it isn't mistaken for a button.
- **Icons.** Material Symbols Sharp, outline, weight 300, grade 0, optical size matched to the icon size. Sizes 20px (beside body text), 24px (buttons, navigation, forms), 40px (feature icons). Always with a text label, except universal icons such as menu, which still need an accessible name. Kiwi black, white or the accent (following the colour pairings above).
- **Logo.** Supplied files only. Clear space equal to the height of the wordmark on every side. Minimum widths on screen: strap right 140px, strap beneath 120px, primary 60px.
- **Logos.** Client logos are single colour (white on dark, Kiwi black on white). They can take the accent on hover.
- **Logo on images.** A soft Kiwi black gradient behind it, or the corner lock-up (a black box with a border a quarter of the logo's height).
- **No generic filler.** No stock icons in grids, no "three benefits" cards and no placeholder testimonials. If content is missing, mark it [TBC].

## 8. Images

- **Treatments.** Standard colour for projects. Mono for atmosphere and behind type. The colour window for a hero moment, once per page. The grid overlay for a feature image.
- **Text on photos** always has a scrim: Kiwi black, at least 0.9 opacity at the text edge, fading out. Test with the brightest photo the slot could hold.
- **Alt text** on every content image, saying what and where ("JD Gyms, Wythenshawe: gym floor with spin bikes"). Decorative images, cells and slices get empty alt text or `aria-hidden`.
- **Formats.** WebP or AVIF, served at the size used, with `srcset`. Hero no wider than 2400px. Cards and grid images no wider than 1200px.
- **Loading.** The hero image loads first. Everything below the first screen lazy-loads.
- **Crops.** Set a focal point for each photo so it crops well from 21:9 down to 4:3 on mobile.

## 9. Motion

- **Character.** Eased, smooth and on the grid. Load in, respond to the cursor, settle. Premium, not showy.
- **Easing.** Ease out `cubic-bezier(.2,.7,.2,1)` for entrances and hovers. Ease in-out `cubic-bezier(.65,0,.35,1)` for transitions between states.
- **Durations.** Use the timing table in the kit. Hovers 200 to 300ms, reveals 600 to 900ms, nothing over 1.5s except loops and parallax.
- **One lead motion per section.** At most one supporting motion with it. No more than two things moving on screen at once, apart from parallax.
- **Animate only transform, opacity and clip-path.** Never animate width, height, top or left on page content.
- **Only while visible.** Loops, intervals and parallax run only while their section is on screen and pause otherwise.
- **No scroll-jacking.** Scrolling always moves the page. No pinned horizontal scroll, no zoom on scroll.
- **Hover is an extra.** Cursor effects (colour windows, gravitate, scatter, previews) run only on devices with a fine pointer that can hover. Nothing important is only available on hover.
- **Pause control.** Anything that moves on its own for more than 5 seconds (logo scrollers, logo columns, crossfades, colour windows) needs a visible pause control on the live site, not only pause on hover. This is WCAG 2.2.2.
- **Reduced motion.** With `prefers-reduced-motion`, every animation shows its final state, loops stop and parallax is off.
- **No flashing.** Nothing flashes more than 3 times a second.

## 10. Accessibility (WCAG 2.2 AA)

- **Contrast.**
  - Body text 4.5:1.
  - Large text (24px, or 18.66px at weight 600 and above) 3:1.
  - UI parts and meaningful graphics 3:1.
  - Check every accent, not just the current one.
- **Focus.** Every interactive element has a visible focus state, at least a 2px outline that contrasts with its background. Never `outline: none` without a replacement.
- **Keyboard.** Everything works with the keyboard alone, in a sensible order. Menus open, close with Escape, and return focus to the button.
- **Targets.** At least 24 × 24px, aiming for 44 × 44px on mobile.
- **Headings.** One H1 per page. Headings in order, never skipping a level for size.
- **Split text.** When a headline is split into words or letters for motion, the full sentence stays readable to screen readers (an `aria-label` on the parent, `aria-hidden` on the pieces).
- **Links and buttons.** Links go somewhere, buttons do something. Labels make sense on their own ("View JD Gyms project", not "Click here").
- **Forms.** Visible labels, errors in text not only colour, and the contact form works without JavaScript.
- **Language.** `lang="en-GB"` on every page.

## 11. Performance

- **Targets on a mid-range phone over 4G:** Largest Contentful Paint under 2.5s, Cumulative Layout Shift under 0.1, Interaction to Next Paint under 200ms.
- **Page weight:** under 1.5MB on first load for the homepage, excluding lazy-loaded images.
- **Fonts.** Two families, only the weights used, subset and self-hosted, with `font-display: swap`.
- **Icons.** The Material Symbols font is subset to the icons used.
- **JavaScript.** One shared IntersectionObserver for visibility. One `requestAnimationFrame` loop per effect, stopped when idle. No library for anything a few lines of code can do.
- **Never store images in CSS custom properties.** It slowed the kit badly.
- **Reserve space** for every image and embed with width and height or `aspect-ratio`, so nothing shifts as it loads.

## 12. Code rules

- **Tokens only.** Colours, sizes, spacing, radii, easing and durations come from `tokens.css`, mirrored in `theme.json` so WordPress only offers brand values.
- **Prefixed class names per block** (`kw-hero__title`). Short shared names like `.hl`, `.ul` or `.mini` clashed in the kit and broke demos.
- **Container queries** for components, so a block works in any column. Mobile layout below 720px container width.
- **Semantic HTML first.** `nav`, `header`, `main`, `section`, `figure`, `button`. ARIA only where HTML can't do it.
- **No inline styles** except for per-item values set by JavaScript.
- **Progressive enhancement.** Content and links work before JavaScript runs. Motion is added on top.
- **One block, one folder.** Markup, styles, script and a short readme with its rules and states.

## 13. Checklists

### Before a section goes to Toby

- [ ] Matches its kit figure and the rules above
- [ ] Desktop 1440px and mobile 390px, no sideways scroll
- [ ] All five accents checked, contrast passes in each
- [ ] Light and dark page themes checked where the section sits on the page background
- [ ] Reduced motion checked
- [ ] Keyboard only: reachable, visible focus, sensible order
- [ ] No hard-coded colours, sizes or timings
- [ ] Every claim and name traces to the copy deck. Open items marked [TBC]
- [ ] Alt text written
- [ ] No console errors

### Before launch

- [ ] Every item in section 1 settled
- [ ] Accessibility review across all templates, including a screen reader pass
- [ ] Core Web Vitals within targets on the real staging server
- [ ] Original photos in place, credited to the right projects
- [ ] Client logo permissions confirmed
- [ ] Pause controls on all auto-moving content
- [ ] Redirects, metadata, sitemap, analytics and cookie consent in place
- [ ] Contact form tested end to end

## 14. Prompt preamble for Claude Design and Claude Code

Paste this at the start of every design or build session:

> Kiwi website. Before generating, read `kiwi-website-rules.md`, the reference kit page and `tokens.css`. Follow them as hard rules. Use tokens only, square corners, Familjen Grotesk and Inter, the accent through `--acc` variables only. Use real copy from the copy deck and mark gaps [TBC]. Never invent figures, clients, quotes or project names. Build one self-contained section at a time and show it at 1440px and 390px. Make small targeted edits to approved sections, never regenerate them. If a rule doesn't cover something, ask before deciding.
