# Chandrama Ritual – Shopify Theme Setup

## Requirements
- Shopify OS 2.0 theme
- GSAP (cdn.jsdelivr.net/npm/gsap)

## Setup
1. Upload section files into /sections
2. Add gsap CDN to theme.liquid before </body>
3. Enable sections in Customize > Homepage
4. Disable unused animations on mobile

## Animation Rules
- Do not add bounce or fast easing
- Keep durations above 0.6s
- Respect prefers-reduced-motion

## Editing Content
All text is editable via Shopify Customizer.
Do not hardcode copy unless specified.

## Performance
- Images unchanged
- Lazy load enabled
- GSAP runs only on desktop
