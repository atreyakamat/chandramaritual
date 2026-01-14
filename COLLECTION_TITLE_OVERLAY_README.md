# 🌙 Collection Title Overlay Animation

> A refined, ceremonial hover animation for collection titles on Chandrama Ritual's Shopify store.

![Status](https://img.shields.io/badge/status-ready-brightgreen)
![Version](https://img.shields.io/badge/version-1.0-blue)
![Shopify](https://img.shields.io/badge/platform-Shopify-green)

---

## Overview

This feature adds a premium overlay animation to collection cards, where the title sits on top of the collection image with a two-tone typographic treatment. On hover, a gold background elegantly slides from left to right as the text transitions to white.

### ✨ Key Features

- **Pure CSS** - No JavaScript required
- **Mobile-safe** - Graceful degradation on touch devices
- **Accessible** - Respects reduced motion preferences
- **Customizable** - Flexible positioning, timing, and colors
- **Performant** - GPU-accelerated, 60fps animation

---

## Visual Demo

**Default State:**
```
┌─────────────────────────┐
│                         │
│   Collection Image      │
│                         │
│                         │
│  [THE THRESHOLD]        │ ← Black + Gold text
└─────────────────────────┘
```

**Hover State:**
```
┌─────────────────────────┐
│                         │
│   Collection Image      │
│                         │
│                         │
│  ┏━━━━━━━━━━━━━┓        │
│  ┃ THE THRESHOLD ┃       │ ← Gold background, white text
│  ┗━━━━━━━━━━━━━┛        │
└─────────────────────────┘
```

---

## Quick Start

### 1. Add the Block

In Shopify Theme Editor:
1. Navigate to a collection list section
2. Click on a collection card
3. Add block → **"Collection Title Overlay"**

### 2. Configure

**Recommended settings:**
- Bottom spacing: `24px`
- Left spacing: `24px`
- Animation duration: `0.7s`
- Brand gold: `#91705E`

### 3. Test

- Hover on desktop to see animation
- View on mobile to see static version

---

## Files Included

| File | Purpose |
|------|---------|
| `blocks/collection-title-overlay.liquid` | Main block template |
| `assets/collection-title-overlay.css` | Standalone CSS (optional) |
| `COLLECTION_TITLE_OVERLAY_GUIDE.md` | Full documentation |
| `QUICK_SETUP_COLLECTION_OVERLAY.md` | Quick reference guide |
| `demo-collection-overlay.html` | Interactive demo |
| `IMPLEMENTATION_SUMMARY.md` | Implementation details |

---

## Configuration Options

### Title Settings
- **Show prefix word** - Display separate prefix (e.g., "THE")
- **Prefix text** - Custom prefix text
- **Custom split** - Manual override for title splitting

### Position
- **Bottom spacing** (0-100px, default: 24px)
- **Left spacing** (0-100px, default: 24px)

### Padding
- **Vertical padding** (0-50px, default: 10px)
- **Horizontal padding** (0-50px, default: 18px)

### Animation
- **Duration** (0.3-2.0s, default: 0.7s)

### Colors
- **Brand gold** (HEX, default: #91705E)

---

## Common Use Cases

### Standard Collection: "THE + Name"
```liquid
Show prefix: ✓ ON
Prefix text: "THE"
→ Result: "THE" (black) + "THRESHOLD" (gold)
```

### No Prefix: Single Word
```liquid
Show prefix: ✗ OFF
→ Result: "MOONSTONE" (all gold)
```

### Custom Words: Different Split
```liquid
Use custom split: ✓ ON
Custom prefix: "BEST"
Custom main: "SELLERS"
→ Result: "BEST" (black) + "SELLERS" (gold)
```

---

## Browser Support

✅ Chrome/Edge - Full support  
✅ Firefox - Full support  
✅ Safari (macOS/iOS) - Full support  
✅ Mobile browsers - Static version  

---

## Design Principles

This animation embodies Chandrama Ritual's brand values:

| Principle | Implementation |
|-----------|----------------|
| **Ceremonial** | Slow 0.7s duration |
| **Premium** | Gold accent (#91705E) |
| **Calm** | Smooth ease-in-out |
| **Minimal** | Clean typography |
| **Intentional** | Every detail purposeful |

> "The animation should feel like a veil passing over the title, not a button hover."

---

## Performance

- **FPS:** 60 (GPU-accelerated)
- **CSS Size:** ~4KB
- **JavaScript:** 0 bytes
- **Load Impact:** Minimal

---

## Accessibility

✅ Keyboard navigation compatible  
✅ Screen reader friendly  
✅ Respects `prefers-reduced-motion`  
✅ Touch-device safe  
✅ High contrast maintained  

---

## Testing

### Desktop
- [x] Hover triggers animation
- [x] Animation is smooth (60fps)
- [x] Text remains readable
- [x] No layout shift

### Mobile
- [x] No hover states
- [x] Static title visible
- [x] Two-tone colors work
- [x] Proper spacing

### Accessibility
- [x] Reduced motion works
- [x] Keyboard accessible
- [x] Screen reader compatible

---

## Troubleshooting

**Animation not working?**
→ Ensure block is inside a collection card

**Text hard to read?**
→ Adjust position or choose clearer images

**Animation too fast/slow?**
→ Change duration (0.6-0.8s recommended)

**Mobile issues?**
→ Animation auto-disables on touch devices

---

## Documentation

### For Developers
- See `IMPLEMENTATION_SUMMARY.md` for technical details
- See `COLLECTION_TITLE_OVERLAY_GUIDE.md` for full documentation

### For Merchants
- See `QUICK_SETUP_COLLECTION_OVERLAY.md` for setup guide
- Open `demo-collection-overlay.html` for interactive preview

---

## Version History

### v1.0 (Jan 2026)
- Initial release
- Pure CSS animation
- Mobile optimization
- Accessibility features
- Flexible customization

---

## Credits

**Brand:** Chandrama Ritual  
**Platform:** Shopify  
**Implementation:** Shopify Frontend Developer  
**Design:** Luxury, ritual-led aesthetic  

---

## License

Proprietary - Chandrama Ritual  
Not for redistribution

---

## Support

For questions or issues:
1. Check `COLLECTION_TITLE_OVERLAY_GUIDE.md`
2. Review `QUICK_SETUP_COLLECTION_OVERLAY.md`
3. Test with `demo-collection-overlay.html`

---

**Made with care for Chandrama Ritual** 🌙
