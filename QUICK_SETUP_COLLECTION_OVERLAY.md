# Collection Title Overlay - Quick Setup Guide

## Quick Start (3 Steps)

### Step 1: Add the Block
1. Open Shopify Theme Editor
2. Navigate to a collection list section (Homepage or Collections page)
3. Click on a Collection Card
4. Click "Add block" → Select **"Collection Title Overlay"**

### Step 2: Position & Style
Use these recommended settings for a premium look:

**Position:**
- Bottom spacing: `24px`
- Left spacing: `24px`

**Padding:**
- Vertical: `10px`
- Horizontal: `18px`

**Animation:**
- Duration: `0.7s` (slow and ceremonial)

### Step 3: Test
- Preview on desktop (hover to see animation)
- Preview on mobile (should show static title with two-tone colors)

---

## Common Setups

### Setup 1: "THE + Collection Name"
**Example:** "THE THRESHOLD"

Settings:
- ✓ Show prefix word: **ON**
- Prefix text: `THE`
- Custom split: **OFF**

Result: 
- "THE" in **black**
- "THRESHOLD" in **gold**
- Hover: Both turn **white** with gold background

---

### Setup 2: Custom Prefix
**Example:** "NEW ARRIVALS"

Settings:
- ✓ Show prefix word: **ON**
- Prefix text: `NEW`
- Custom split: **OFF**

Result:
- "NEW" in **black**
- "ARRIVALS" in **gold**

---

### Setup 3: No Prefix (All Gold)
**Example:** "MOONSTONE"

Settings:
- Show prefix word: **OFF**
- Custom split: **OFF**

Result:
- "MOONSTONE" in **gold**

---

### Setup 4: Advanced Custom Split
**Example:** Collection title is "Best Sellers" but you want "SHOP" + "BEST SELLERS"

Settings:
- Show prefix word: _doesn't matter_
- ✓ Use custom title split: **ON**
- Custom prefix: `SHOP`
- Custom main text: `BEST SELLERS`

Result:
- "SHOP" in **black**
- "BEST SELLERS" in **gold**

---

## Troubleshooting

### Problem: Title doesn't show
**Check:** Is the block inside a Collection Card block?

### Problem: No animation on hover
**Check:** 
- Are you on desktop? (No hover on mobile by design)
- Is animation duration > 0?

### Problem: Text hard to read
**Solution:** Adjust position to avoid busy areas of image, or choose different collection images

### Problem: Title too long
**Solution:** 
- Reduce horizontal padding
- Use shorter collection names
- Or hide the prefix for that specific card

---

## Brand Colors

- **Brand Gold:** `#91705E` (default)
- **Black:** `#000000` (prefix)
- **White:** `#FFFFFF` (hover state)

---

## Mobile Behavior

On mobile devices (phones & tablets):
- ✓ Title remains visible
- ✓ No hover animation (touch-safe)
- ✓ Text uses default two-tone colors
- ✓ Slightly smaller font size
- ✓ Slightly reduced spacing

This ensures the experience is native to touch devices!

---

## Animation Timing Guide

| Duration | Feel | Best For |
|----------|------|----------|
| 0.3-0.5s | Quick, playful | Not recommended for Chandrama |
| **0.6-0.8s** | **Slow, ceremonial** | ✓ **Recommended** |
| 0.9-1.2s | Very slow | Large hero sections |
| 1.3-2.0s | Ultra-slow | Special emphasis only |

---

## Multiple Collection Cards

To apply the same styling across all collection cards:

1. Add the block to the **first** collection card
2. Configure your settings
3. **Copy the block** (in theme editor)
4. **Paste** into other collection cards
5. Adjust custom splits if needed per collection

---

## Best Practices

✓ **DO:**
- Use consistent positioning across all cards
- Choose images with space in bottom-left corner
- Test on both desktop and mobile
- Keep animation between 0.6-0.8s

✗ **DON'T:**
- Don't use images with text in bottom-left
- Don't make the animation too fast (<0.5s)
- Don't override font-family or text-transform
- Don't forget to test on mobile

---

**Need Help?** See `COLLECTION_TITLE_OVERLAY_GUIDE.md` for detailed documentation.
