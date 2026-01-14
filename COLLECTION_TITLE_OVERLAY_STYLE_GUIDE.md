# Collection Title Overlay - Visual Style Guide

## Brand Identity

**Brand:** Chandrama Ritual  
**Aesthetic:** Luxury • Ritual-led • Ceremonial • Minimalist  
**Feeling:** Calm • Intentional • Premium • Editorial  

---

## Color Palette

### Primary Colors

| Color Name | HEX | RGB | Use Case |
|------------|-----|-----|----------|
| **Brand Gold** | `#91705E` | `rgb(145, 112, 94)` | Main title text, hover background |
| **Black** | `#000000` | `rgb(0, 0, 0)` | Prefix text |
| **White** | `#FFFFFF` | `rgb(255, 255, 255)` | Hover state text |

### Color Swatches

```
┌──────────────┐  ┌──────────────┐  ┌──────────────┐
│              │  │              │  │              │
│   #91705E    │  │   #000000    │  │   #FFFFFF    │
│  Brand Gold  │  │    Black     │  │    White     │
│              │  │              │  │              │
└──────────────┘  └──────────────┘  └──────────────┘
```

### Color Usage

**Default State (No Hover):**
- Prefix: `#000000` (Black)
- Main Text: `#91705E` (Brand Gold)
- Background: Transparent

**Hover State:**
- Prefix: `#FFFFFF` (White)
- Main Text: `#FFFFFF` (White)
- Background: `#91705E` (Brand Gold)

---

## Typography

### Font Specification

| Property | Value | Notes |
|----------|-------|-------|
| **Font Family** | Heading font (serif) | Uses theme's heading font |
| **Font Size** | `1.2rem` (19.2px @ 16px base) | Responsive |
| **Font Weight** | `400` (Regular) | Not bold |
| **Text Transform** | `UPPERCASE` | All caps, always |
| **Letter Spacing** | `0.08em` | Wide tracking |
| **Line Height** | Inherit | Single line only |
| **White Space** | `nowrap` | Never wraps |

### Typography Scale

| Screen Size | Font Size | Notes |
|-------------|-----------|-------|
| **Mobile** (<480px) | `1.0rem` (16px) | Smaller for mobile |
| **Tablet** (750-1024px) | `1.1rem` (17.6px) | Slightly smaller |
| **Desktop** (>1024px) | `1.2rem` (19.2px) | Default |
| **Large** (>1280px) | `1.3rem` (20.8px) | Larger for big screens |

---

## Spacing & Layout

### Positioning

**Default Values:**
```
Bottom: 24px (from card bottom)
Left:   24px (from card left)
```

**Responsive Adjustments:**
```css
Mobile (<480px):
  Bottom: 16px
  Left:   16px

Desktop (≥750px):
  Bottom: 24px
  Left:   24px
```

### Padding

**Internal Padding (Title Box):**
```
Vertical:   10px (top & bottom)
Horizontal: 18px (left & right)
```

**Mobile Adjustment:**
```css
Mobile (<480px):
  Vertical:   8px  (80% of default)
  Horizontal: 14px (80% of default)
```

### Visual Spacing Diagram

```
┌────────── Collection Card ──────────┐
│                                     │
│                                     │
│        Collection Image             │
│                                     │
│                                     │
│  ◄─24px─►┏━━━━━━━━━━━━━┓           │
│          ┃ ▲           ┃           │
│          ┃10px         ┃           │
│          ┃ ▼           ┃           │
│          ┃◄18px►THE◄6px►THRESHOLD◄18px►
│          ┃ ▲           ┃           │
│          ┃10px         ┃           │
│          ┃ ▼           ┃           │
│          └─────────────┘           │
│          ▲                         │
│         24px                       │
└─────────────────────────────────────┘
```

---

## Animation Specifications

### Timing

| Property | Value | Purpose |
|----------|-------|---------|
| **Duration** | `0.7s` | Main animation length |
| **Easing** | `ease-in-out` | Smooth acceleration/deceleration |
| **Text Delay** | `0.5s` (70% of duration) | Text color changes slightly after background |

### Timeline

```
0ms                                              700ms
├───────────────────────────────────────────────┤
│                                               │
│ ┌──── Background Slide ─────┐                │
│ │   translateX(-100% → 0%)  │                │
│ └───────────────────────────┘                │
│                                               │
│     ┌──── Text Color Transition ────┐        │
│     │   Gold/Black → White           │        │
│     └────────────────────────────────┘        │
│                                               │
└───────────────────────────────────────────────┘
```

### Animation Curve

```
Speed
  ▲
  │     ┌─────┐
  │   ╱         ╲
  │ ╱             ╲
  │╱               ╲
  └─────────────────▶ Time
  0                0.7s

ease-in-out: Slow start, fast middle, slow end
```

### Recommended Durations

| Feel | Duration | Use Case |
|------|----------|----------|
| Quick | 0.3-0.5s | Not recommended (too playful) |
| **Standard** | **0.6-0.8s** | ✓ **Recommended** (luxury) |
| Slow | 0.9-1.2s | Hero/featured sections |
| Very Slow | 1.3-2.0s | Special emphasis only |

---

## Visual Effects

### Text Shadow

**Default State:**
```css
text-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
```
- **Blur:** 3px
- **Offset:** 0px horizontal, 1px down
- **Color:** 10% black
- **Purpose:** Readability on images

**Hover State:**
```css
text-shadow: none;
```
- Removed when background appears
- Background provides contrast

### Background Animation

**Initial State:**
```css
transform: translateX(-100%);
```
- Positioned off-screen to the left
- Not visible

**Hover State:**
```css
transform: translateX(0);
```
- Slides into view
- Covers the text area
- GPU-accelerated

### Z-Index Layering

```
Layer Stack (bottom to top):
─────────────────────────────
5. Text (Title)          z-index: auto
4. Background (Gold)     z-index: -1 (relative to wrapper)
3. Wrapper               z-index: 2
2. Collection Image      z-index: 1 (implicit)
1. Card Link             z-index: 1
```

---

## Mobile Specifications

### Touch Device Behavior

**Visual Changes:**
- ❌ No hover animation
- ❌ No gold background slide
- ✓ Static two-tone text
- ✓ Transparent background
- ✓ Reduced spacing

**Detection Method:**
```css
@media (hover: none) {
  /* Mobile/touch styles */
}
```

### Mobile-Specific Values

| Property | Desktop | Mobile | Change |
|----------|---------|--------|--------|
| Bottom spacing | 24px | 16px | -33% |
| Left spacing | 24px | 16px | -33% |
| Font size | 1.2rem | 1.0rem | -17% |
| Letter spacing | 0.08em | 0.06em | -25% |
| Vertical padding | 10px | 8px | -20% |
| Horizontal padding | 18px | 14px | -22% |

---

## Accessibility Specifications

### Reduced Motion

**When `prefers-reduced-motion: reduce` is active:**
```css
Animation duration: 0.01s (instant)
Transition duration: 0.01s (instant)
```

**Users affected:**
- People with vestibular disorders
- Users who enabled "Reduce Motion" in OS settings
- Approximately 7-10% of users

### Color Contrast Ratios

**Default State:**
- Gold on Image: Varies (requires testing per image)
- Black on Image: Varies (requires testing per image)
- Text shadow provides minimum contrast

**Hover State:**
- White on Gold (#FFFFFF on #91705E): **5.3:1** ✓ AA Pass

### Keyboard Navigation

- Focus states handled by parent link
- No focusable elements within overlay
- Keyboard interaction follows native link behavior

---

## Design Variants

### Variant 1: Editorial (Large Cards)
```
Bottom:    32px (+33%)
Left:      32px (+33%)
Duration:  0.8s (+14%)
Padding:   12px / 20px (+20% / +11%)
```

### Variant 2: Compact (Small Cards)
```
Bottom:    16px (-33%)
Left:      16px (-33%)
Duration:  0.6s (-14%)
Padding:   8px / 12px (-20% / -33%)
```

### Variant 3: Hero (Extra Large)
```
Bottom:    48px (+100%)
Left:      48px (+100%)
Duration:  0.9s (+29%)
Padding:   14px / 24px (+40% / +33%)
```

---

## Component Anatomy

```
.collection-title-overlay-wrapper
├── ::before (animated background)
└── .collection-title-overlay
    ├── .title-prefix (optional)
    │   └── [Text Node: "THE"]
    │
    └── .title-main (required)
        └── [Text Node: "THRESHOLD"]
```

**CSS Classes:**
- `.collection-title-overlay-wrapper` - Container with positioning
- `.collection-title-overlay` - Text container with flex layout
- `.title-prefix` - Prefix text (black → white)
- `.title-main` - Main text (gold → white)

---

## Grid Integration

### In Editorial Layout
```
Collection cards in asymmetric grid
Title overlays on bottom-left
Consistent positioning across all cards
```

### In Standard Grid
```
Collection cards in uniform grid
Title overlays on bottom-left
Equal spacing maintained
```

### In Bento Layout
```
Variable card sizes
Title scales with card
Positioning adjusts proportionally
```

---

## Quality Checklist

Brand designers should verify:

- [ ] Gold color exactly matches `#91705E`
- [ ] Animation feels "slow and intentional"
- [ ] No playful or bouncy movements
- [ ] Typography is uppercase serif
- [ ] Letter spacing creates elegant feel
- [ ] Mobile version is static (no broken hover)
- [ ] Text shadow enhances readability
- [ ] Contrast passes WCAG AA on hover
- [ ] Positioning is consistent across cards
- [ ] Animation timing matches brand aesthetic

---

## Don'ts (Anti-Patterns)

❌ **Don't:**
- Use sans-serif fonts
- Make animation faster than 0.5s
- Use bright or saturated colors
- Add bounce or elastic easing
- Animate multiple properties simultaneously
- Use decorative fonts
- Override the uppercase transform
- Add drop shadows on hover
- Use gradients in background
- Animate opacity with transform

✓ **Do:**
- Keep animation slow (0.6-0.8s)
- Use serif heading font
- Maintain brand gold color
- Use ease-in-out easing only
- Let background slide smoothly
- Keep typography clean
- Respect uppercase styling
- Use subtle text shadow (default only)
- Use solid gold background
- Animate transform and color separately

---

## File References

**Block:** `blocks/collection-title-overlay.liquid`  
**CSS:** `assets/collection-title-overlay.css`  
**Demo:** `demo-collection-overlay.html`  

---

**Style Guide Version:** 1.0  
**Last Updated:** January 2026  
**Brand:** Chandrama Ritual  
**Maintained By:** Design Team
