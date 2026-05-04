# Joeri Billast — Design System Reference

> **For Claude Code / AI assistants:** This file defines the complete design system for Joeri Billast's personal brand website. Use it as the authoritative reference when building, refining, or generating any UI for this project.

---

## Brand Identity

| | |
|---|---|
| **Full name** | Joeri Billast |
| **Tagline** | The Future CMO |
| **Role** | Fractional CMO · AI Visibility Strategist · Keynote Speaker |
| **Tone** | Strategic advisor — calm, authoritative, forward-looking |
| **Visual language** | Stripe / Apple / Claude — minimal, premium, type-driven |

---

## Design Principles

1. **Type and space carry authority.** Color is not the storyteller — whitespace and typography are.
2. **One accent color.** Purple (`#5b3fcf`) is the only interactive color. No secondary accents.
3. **Weight 300 for all display.** Headlines, subheadings, body copy — all weight 300. Buttons and labels are weight 400.
4. **Neutral shadows.** No blue-tinted shadows. Pure `rgba(0,0,0,...)` layers only.
5. **No decorative gradients.** The brand dark (`#2d1b69`) is the only "bold" visual moment.
6. **Generous whitespace.** Section padding: 96–120px. Line-height: 1.65 for body.

---

## Color Tokens

### Neutrals

| Token | Value | Use |
|---|---|---|
| `--color-heading` | `#111118` | All headings, strong text |
| `--color-label` | `#2c2c35` | Form labels, secondary headings |
| `--color-body` | `#6b7280` | Body text, descriptions |
| `--color-muted` | `#9ca3af` | Placeholders, metadata, eyebrows |
| `--color-border` | `#e8e8ed` | All borders and dividers |
| `--color-border-light` | `#f0f0f5` | Hairline dividers inside cards |
| `--color-surface` | `#f5f5f7` | Section backgrounds (Apple-style) |
| `--color-off-white` | `#fafafa` | Alternate page bg, footer |
| `--color-white` | `#ffffff` | Page bg, card surfaces |

### Brand Purple (single accent)

| Token | Value | Use |
|---|---|---|
| `--color-purple` | `#5b3fcf` | CTAs, links, active states |
| `--color-purple-hover` | `#4a32b0` | Hover on purple elements |
| `--color-purple-active` | `#3d2899` | Press / active state |
| `--color-purple-light` | `#ede9fc` | Badge fill, ghost button bg |
| `--color-purple-border` | `#c4b8f5` | Ghost button border, input focus ring |
| `--color-purple-muted` | `#9b8ed4` | Subdued purple, taglines |
| `--color-brand-dark` | `#2d1b69` | Dark section backgrounds only |
| `--color-wordmark-name` | `#1e1654` | "JOERI BILLAST" in wordmark |
| `--color-wordmark-tag` | `#7b5ea7` | "The Future CMO" in wordmark |

### System States (never decorative)

| Token | Value | Use |
|---|---|---|
| `--color-success` | `#16a34a` | Success text |
| `--color-success-bg` | `#f0fdf4` | Success background |
| `--color-success-border` | `#bbf7d0` | Success border |
| `--color-error` | `#dc2626` | Error text |
| `--color-error-bg` | `#fef2f2` | Error background |
| `--color-error-border` | `#fecaca` | Error border |

**Do not use:** ruby (`#ea2261`), magenta (`#f96bee`), green (`#15be53`) as brand or decorative colors.

---

## Typography

### Font Stack

```css
--font-primary: 'DM Sans', 'SF Pro Display', system-ui, sans-serif;
--font-mono:    'Source Code Pro', 'SFMono-Regular', monospace;
```

> ⚠️ **Production note:** `sohne-var` (Klim Type Foundry) is the intended primary font. `DM Sans` is the design-system substitute. When `sohne-var` .woff2 files are available, add a `@font-face` block and update `--font-primary`.

### OpenType Features

```css
font-feature-settings: "ss01";   /* Always — on all text */
font-feature-settings: "tnum";   /* For numeric/financial data only */
```

### Type Scale

| Role | Size | Weight | Line-height | Letter-spacing |
|---|---|---|---|---|
| Hero / H1 | 56px (3.5rem) | 300 | 1.04 | −1.5px |
| H1 | 48px (3rem) | 300 | 1.10 | −1.0px |
| H2 / Section | 32px (2rem) | 300 | 1.15 | −0.6px |
| H3 / Subheading | 26px (1.625rem) | 300 | 1.20 | −0.3px |
| H4 | 22px (1.375rem) | 300 | 1.25 | −0.2px |
| Body Large | 18px (1.125rem) | 300 | 1.65 | — |
| Body | 16px (1rem) | 300 | 1.65 | — |
| UI / Button | 15px (0.9375rem) | 400 | 1.0 | — |
| Label / Link | 14px (0.875rem) | 400 | — | — |
| Caption | 13px (0.8125rem) | 400 | — | — |
| Small | 12px (0.75rem) | 400 | 1.5 | — |
| Micro / Eyebrow | 11px (0.6875rem) | 500 | — | 0.04em + uppercase |
| Code | 13px (0.8125rem) | 500 | 1.8 | — |

**Rules:**
- Weight 300 for all content text (headings + body)
- Weight 400 for interactive UI only (buttons, nav, labels, links)
- Weight 500 for eyebrow labels and code
- Never use weight 600+ in the UI

---

## Shadow System

Neutral-toned only. No blue tint.

| Token | Value | Use |
|---|---|---|
| `--shadow-0` | `none` | Flat / no elevation |
| `--shadow-1` | `0 1px 3px rgba(0,0,0,.06), 0 1px 2px rgba(0,0,0,.04)` | Ambient lift |
| `--shadow-2` | `0 4px 6px -1px rgba(0,0,0,.07), 0 2px 4px -1px rgba(0,0,0,.04)` | Standard card ★ |
| `--shadow-3` | `0 10px 30px -8px rgba(0,0,0,.12), 0 4px 8px -2px rgba(0,0,0,.06)` | Elevated / hover |
| `--shadow-4` | `0 20px 48px -12px rgba(0,0,0,.18), 0 8px 16px -4px rgba(0,0,0,.08)` | Modal / floating |
| `--shadow-focus` | `0 0 0 3px rgba(91,63,207,.18)` | Keyboard focus ring |

---

## Border Radius

| Token | Value | Use |
|---|---|---|
| `--radius-micro` | `2px` | Subtle corners |
| `--radius-standard` | `6px` | Buttons, inputs, badges |
| `--radius-comfortable` | `8px` | Standard cards |
| `--radius-relaxed` | `10px` | Larger cards, panels |
| `--radius-large` | `14px` | Feature cards, hero elements |

---

## Spacing Scale (base 8px)

`4 · 6 · 8 · 10 · 12 · 14 · 16 · 20 · 24 · 32 · 40 · 48 · 64 · 80 · 96 · 120 · 160`

Section vertical padding: **96px** minimum. Hero: **120px**.

---

## Components

### Buttons

```css
/* Primary */
background: #5b3fcf; color: #fff;
padding: 10px 22px; border-radius: 6px;
font-size: 15px; font-weight: 400;
hover → background: #4a32b0

/* Ghost (on light bg) */
background: transparent; color: #5b3fcf;
border: 1px solid #5b3fcf; border-radius: 6px;
hover → background: #ede9fc; color: #4a32b0; border-color: #4a32b0

/* Ghost on dark bg */
background: transparent; color: #ffffff;
border: 1px solid #ffffff;
hover → background: rgba(255,255,255,0.10); border stays white (no thickening to avoid layout shift)

/* Neutral */
background: #f5f5f7; color: #2c2c35;
border: 1px solid #e8e8ed;
hover → background: #eeeef3
```

### Badges / Tags

```css
/* Purple (default — use for categories/tags) */
background: #ede9fc; color: #4a32b0;
border: 1px solid #c4b8f5; border-radius: 6px;
font-size: 12px; font-weight: 400; padding: 3px 10px;

/* Success / availability */
background: #f0fdf4; color: #16a34a;
border: 1px solid #bbf7d0;
+ green dot 6px

/* Neutral */
background: #f5f5f7; color: #2c2c35;
border: 1px solid #e8e8ed;

/* Dark */
background: #111118; color: #fff;
```

### Cards

```css
/* Standard */
background: #fff;
border: 1px solid #e8e8ed;
border-radius: 10px;
padding: 28px;
box-shadow: var(--shadow-2);
hover → box-shadow: var(--shadow-3); transform: translateY(-2px);

/* Surface (on off-white bg) */
background: #f5f5f7;
border: 1px solid #e8e8ed;
border-radius: 10px;

/* Dark section */
background: rgba(255,255,255,0.05);
border: 1px solid rgba(255,255,255,0.08);
border-radius: 8px;
```

### Form Inputs

```css
border: 1px solid #e8e8ed;
border-radius: 6px;
padding: 10px 14px;
font-size: 15px; font-weight: 300;
color: #111118; background: #fff;

focus → border-color: #5b3fcf; box-shadow: 0 0 0 3px rgba(91,63,207,0.12);
error → border-color: #dc2626;
disabled → color: #9ca3af; background: #f5f5f7;
```

### Navigation

```css
height: 64px; padding: 0 48px;
background: rgba(255,255,255,0.94);
backdrop-filter: blur(12px);
border-bottom: 1px solid #e8e8ed;

/* Nav links */
font-size: 14px; font-weight: 400; color: #111118;
active → color: #5b3fcf; border-bottom: 2px solid #5b3fcf;
hover → color: #5b3fcf;
```

### Dark Section

```css
background: #2d1b69;
padding: 96px 48px;
/* Headings */ color: #fff; font-weight: 300;
/* Body */ color: rgba(255,255,255,0.60);
/* Inner cards */ background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.08);
```

---

## Logo & Brand Assets

| File | Description | Use |
|---|---|---|
| `assets/logo-full.png` | Full lockup — icon + "JOERI BILLAST / The Future CMO" — **transparent bg** | Nav bar, footer, light backgrounds |
| `assets/logo-icon.png` | Rocket + globe icon only — **transparent bg** | Hero, avatar, dark sections, favicon |
| `assets/logo-full.svg` | SVG vector lockup | Production (scalable) |
| `assets/logo-horizontal.jpg` | On dark purple bg (JPG) | Reference only |
| `assets/logo-square.jpg` | Square on dark purple bg (JPG) | Reference only |

**Logo usage rules:**
- On white / light bg → use `logo-full.png` or `logo-icon.png`
- On dark section (`#2d1b69`) → use `logo-icon.png` only (full PNG has white bg)
- Never add drop shadow to the logo
- Minimum height: 28px for full lockup, 24px for icon only

---

## Layout

| | |
|---|---|
| Max content width | 1080px, centered |
| Page padding (desktop) | 48px horizontal |
| Page padding (mobile) | 24px horizontal |
| Section vertical padding | 96px (min), 120px (hero) |
| Base spacing unit | 8px |
| Section rhythm | White (`#fff`) → Off-white (`#fafafa`) → Dark (`#2d1b69`) → White |
| Nav height | 64px |
| Body max-width (text) | 640px for reading columns |

---

## Motion & Interaction

| Property | Value |
|---|---|
| Transition duration | 160–200ms |
| Easing | `ease-out` for entrances, `ease-in` for exits |
| Card hover | `translateY(-2px)` + shadow deepens |
| Button hover | Background darkens (no scale) |
| Page transitions | `opacity 0→1` + `translateY(6px→0)` over 200ms |
| No | Bounces, springs, scale transforms on press |

---

## Content Voice

- **Tone**: Confident without arrogance. Strategic. Forward-looking.
- **Register**: First-person for personal/about sections. Second-person for client-facing copy.
- **Casing**: Sentence case everywhere. Title case only for proper names.
- **Recurring motif**: "Future" — The Future CMO, future-proof, what's next.
- **No emoji** in UI or copy.
- **No exclamation marks** in body copy.
- **CTAs**: Direct and action-forward — "Get in touch" / "View my work" / "Book a keynote"
- **Section eyebrows**: 11px / 500 / uppercase / `#9ca3af` — use to orient the reader before headings

---

## Page Structure (website)

```
Nav (sticky, blur)
  └── Logo (full lockup) · Work · About · Writing · Contact · [Get in touch]

Home
  └── Hero (white, 120px padding)
        Logo icon · Available badge · Name · Tagline · Description · CTAs
  └── Feature Section (off-white #fafafa, 96px padding)
        Eyebrow · H2 · 3-column project cards
  └── Dark Section (#2d1b69, 96px padding)
        2-column: headline/copy/CTAs + 3 capability cards

Work     → 2-col grid of project cards
About    → 2-col: avatar/badge + bio/expertise badges
Writing  → Single column list, row-per-post with hover indent
Contact  → Single column form (name, email, message)

Footer (off-white #fafafa)
  └── Logo · Nav links · Copyright
```

---

## CSS File

All tokens live in `colors_and_type.css` at the project root. Import it in any HTML file:

```html
<link rel="stylesheet" href="/colors_and_type.css">
```

Or reference relative to file location.

---

## What NOT to do

- ❌ Blue-tinted shadows (`rgba(50,50,93,...)`) — use neutral `rgba(0,0,0,...)` only
- ❌ Blue-gray body text (`#64748d`) — use warm gray `#6b7280`
- ❌ Blue-tinted borders (`#e5edf5`) — use neutral `#e8e8ed`
- ❌ Old purple (`#533afd`) — use `#5b3fcf`
- ❌ Ruby / magenta as brand colors
- ❌ Green as a brand color (system states only)
- ❌ Decorative gradients (ruby → magenta)
- ❌ Font weight 600+ anywhere in the UI
- ❌ Pill/rounded buttons (border-radius > 14px on buttons)
- ❌ Dark section background `#1c1e54` — use `#2d1b69`
- ❌ Emoji in the UI
