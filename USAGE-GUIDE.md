# Partner Model Interactive Animation - Usage Guide

## Overview

This interactive animation displays Marketing Partners' 3-layer Partner Model with hover effects, click navigation, progress tracking, and responsive design. The model features three layers: Positionering (foundation), Strategie (route), and Activatie (execution).

## Files

- `index.html` - Complete standalone HTML file ready for Elementor embedding
- `font/` - Directory containing Mosafin font files (Bold, SemiBold, Medium)

## Embedding in Elementor

### Method 1: HTML Widget (Recommended)

1. In your Elementor editor, drag an **HTML widget** to your page
2. Open `index.html` in a text editor
3. Copy the **entire content** (everything between and including `<html>` and `</html>`)
4. Paste it into the HTML widget
5. Update and preview your page

**Note:** Ensure the font files are uploaded to your server and accessible via the `font/` directory relative to the HTML file location.

### Method 2: Shortcode (If using Elementor Pro)

1. Create a shortcode in your theme's functions.php or a custom plugin
2. Return the HTML content from the file
3. Use `[partner_model]` shortcode in your Elementor widget

### Method 3: Full Screen Integration

The animation is designed to work in full-screen mode (`height: 100svh`) and can be integrated as a standalone page or section.

## Customization

### Changing Colors

All colors are defined as CSS variables at the top of the `<style>` section:

```css
:root {
  --midnight-indigo: #1d194b;
  --lavender-mist: #a2acd8;
  --neutral-grey: #c8c8c8;
  --white: #ffffff;
  --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}
```

Simply update these values to change the color scheme.

### Changing Fonts

The animation uses two font families:

- **Mosafin** (custom font) - For headings (h1-h6)
- **Rethink Sans** (Google Font) - For paragraphs

Custom Mosafin font files are loaded from the `font/` directory:

- Mosafin-Bold (700 weight)
- Mosafin-SemiBold (600 weight)
- Mosafin-Medium (500 weight)

### Updating Links

Links are in the SVG `<a>` tags within each layer:

- **Positionering (Layer 3)**: `https://marketing-partners.nl/positionering`
- **Strategie (Layer 2)**: `https://marketing-partners.nl/strategie`
- **Activatie (Layer 1)**: `https://marketing-partners.nl/activatie`

Each link uses the `handleLayerClick()` JavaScript function for smooth navigation with visual feedback.

### Modifying Text

All descriptive text is in the HTML description panels located after the SVG:

**Positionering Panel:**

- Step: "1"
- Subtitle: "De fundering"
- Title: "Positionering"
- Description: Content about brand positioning

**Strategie Panel:**

- Step: "2"
- Subtitle: "De route"
- Title: "Strategie"
- Description: Content about strategic planning

**Activatie Panel:**

- Step: "3"
- Subtitle: "De uitvoering"
- Title: "Activatie"
- Description: Content about execution and campaigns

**Instruction Text:**
Located in `.instruction-text` class: "Beweeg over de lagen om te ontdekken hoe het PartnerModel werkt van fundament tot uitvoering."

## Features

- ✅ **Responsive design** - Adapts to mobile, tablet, and desktop
- ✅ **Smooth hover animations** - Layer lifting effects with shadows
- ✅ **Click navigation** - Direct links to subpages with visual feedback
- ✅ **Progress tracking** - Visual dots show explored layers
- ✅ **Keyboard accessible** - Tab navigation + Enter/Space activation
- ✅ **Touch-friendly** - Mobile touch interaction support
- ✅ **SEO-friendly** - All text in DOM, semantic HTML structure
- ✅ **Custom typography** - Mosafin + Rethink Sans fonts
- ✅ **Staggered animations** - Layers appear with delay (bottom to top)
- ✅ **Interactive descriptions** - Context panels appear on hover/focus
- ✅ **Full-screen design** - Uses 100svh for immersive experience
- ✅ **Brand colors integrated** - Marketing Partners color palette
- ✅ **Lightweight** - No external JavaScript libraries required

## Browser Compatibility

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers

## Performance

- **No external JavaScript libraries** - Pure vanilla JavaScript
- **CSS transitions & animations** - Hardware-accelerated transforms
- **Custom font loading** - Mosafin fonts loaded via @font-face
- **Google Fonts** - Rethink Sans loaded asynchronously
- **Optimized SVG** - Inline SVG for fast loading and styling control
- **Efficient animations** - Uses transform and opacity for 60fps performance

### Font Loading Optimization

For faster loading, you can:

1. Self-host Rethink Sans instead of using Google Fonts
2. Use `font-display: swap` for better loading performance
3. Preload critical font files in the HTML `<head>`

## Accessibility

- **ARIA labels** - Each layer has descriptive `aria-label` attributes
- **Keyboard navigation** - Full Tab + Enter/Space support
- **Focus indicators** - Visual outline on focused elements
- **Semantic HTML** - Proper heading hierarchy and button roles
- **Screen reader friendly** - All text content accessible
- **Touch accessibility** - Large touch targets for mobile users
- **Color contrast** - High contrast ratios for readability

## Troubleshooting

### Descriptions not showing

- Ensure JavaScript is enabled in browser
- Check browser console for errors
- Verify CSS is not being blocked by ad blockers
- Confirm description panels have correct `data-for` attributes

### Fonts not loading

- Verify font files are uploaded to `font/` directory
- Check file permissions on server
- Ensure correct MIME types for font files (.woff2, .ttf)
- Test font loading in browser developer tools

### Links not working

- Check that links are correctly formatted (https://)
- Verify `handleLayerClick()` function is present
- Test in different browsers
- Check if JavaScript is being blocked

### Layout issues

- Check Elementor widget width settings
- Ensure container has sufficient space (minimum 600px width recommended)
- Test responsive breakpoints (1024px, 768px)
- Verify viewport meta tag is present

### Animation performance

- Check if hardware acceleration is enabled in browser
- Reduce motion settings may affect animations
- Test on different devices for performance
- Consider reducing animation complexity for older devices

### Mobile touch issues

- Ensure touch events are not being intercepted
- Test on actual devices, not just browser dev tools
- Check for conflicting touch event handlers
- Verify viewport settings for mobile
