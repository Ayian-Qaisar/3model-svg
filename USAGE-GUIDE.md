# Partner Model Interactive Animation - Usage Guide

## Overview
This interactive animation displays Marketing Partners' 3-layer Partner Model with hover effects and click navigation.

## Files
- `partner-model-interactive.html` - Complete standalone HTML file ready for Elementor embedding

## Embedding in Elementor

### Method 1: HTML Widget (Recommended)
1. In your Elementor editor, drag an **HTML widget** to your page
2. Open `partner-model-interactive.html` in a text editor
3. Copy the **entire content** (everything between and including `<html>` and `</html>`)
4. Paste it into the HTML widget
5. Update and preview your page

### Method 2: Shortcode (If using Elementor Pro)
1. Create a shortcode in your theme's functions.php or a custom plugin
2. Return the HTML content from the file
3. Use `[partner_model]` shortcode in your Elementor widget

## Customization

### Changing Colors
All colors are defined as CSS variables at the top of the `<style>` section:

```css
:root {
    --midnight-indigo: #1D194B;
    --lavender-mist: #A2ACD8;
    --neutral-grey: #C8C8C8;
    --white: #FFFFFF;
}
```

Simply update these values to change the color scheme.

### Updating Links
Links are in the SVG `<a>` tags:
- Positionering: `https://marketing-partners.nl/positionering`
- Strategie: `https://marketing-partners.nl/strategie`
- Activatie: `https://marketing-partners.nl/activatie`

### Modifying Text
All descriptive text is in the HTML description panels:
- Subtitle (e.g., "De fundering")
- Title (e.g., "Positionering")
- Description text

## Features
- ✅ Responsive design (mobile-friendly)
- ✅ Smooth hover animations
- ✅ Click navigation to subpages
- ✅ Keyboard accessible (Tab + Enter)
- ✅ Touch-friendly for mobile devices
- ✅ SEO-friendly (all text in DOM)
- ✅ Lightweight (<50KB without fonts)
- ✅ Brand colors integrated

## Browser Compatibility
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers

## Performance
- No external JavaScript libraries required
- Uses CSS transitions for smooth animations
- Google Fonts (Inter) can be replaced with system fonts for faster loading

## Accessibility
- ARIA labels on interactive elements
- Keyboard navigation support
- Focus indicators
- Semantic HTML structure

## Troubleshooting

### Descriptions not showing
- Ensure JavaScript is enabled
- Check browser console for errors
- Verify CSS is not being blocked

### Links not working
- Check that links are correctly formatted
- Verify onclick handler is present
- Test in different browsers

### Layout issues
- Check Elementor widget width settings
- Ensure container has sufficient space
- Test responsive breakpoints

