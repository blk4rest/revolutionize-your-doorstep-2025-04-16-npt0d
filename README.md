# DoorGaze Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the DoorGaze landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common maintenance tasks.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Main Sections Overview
The landing page consists of these key sections:
- Header (navigation)
- Hero section
- Features section
- Benefits section
- Call-to-action section
- Footer

### Updating Text Content

#### Header/Navigation
```html
<!-- Located in the header section -->
<span class="text-xl font-bold text-blue-600">DoorGaze</span>
```
To change the logo text, simply replace "DoorGaze" with your desired text.

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 tracking-tight mb-6">
    Revolutionize Your Doorstep
</h1>
<p class="text-xl md:text-2xl text-gray-600 max-w-3xl mx-auto mb-12">
    See who's at your door, from anywhere, anytime
</p>
```
Replace the heading and paragraph text while maintaining the existing HTML structure.

### Understanding Tailwind CSS Classes

#### Responsive Design Classes
The page uses these breakpoint prefixes:
- `md:` - Medium screens (768px and up)
- `lg:` - Large screens (1024px and up)

Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
This means:
- Mobile: text-4xl (2.25rem)
- Tablet: text-5xl (3rem)
- Desktop: text-6xl (3.75rem)

#### Common Tailwind Classes Used
- Spacing: `px-4`, `py-24`, `mb-6` (padding and margin)
- Colors: `text-blue-600`, `bg-white`, `text-gray-900`
- Typography: `font-bold`, `text-xl`, `tracking-tight`
- Layout: `flex`, `grid`, `max-w-7xl`

## Fixing Broken Links

### Current Link Structure
```html
<!-- Navigation Links -->
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#guides">Guides</a>
<a href="https://doorgaze.curatedspot.com/">Get Started</a>
```

### Updating Links
1. Internal Links (sections on the same page):
   ```html
   <!-- Format -->
   <a href="#section-id">Link Text</a>
   ```
   
2. External Links:
   ```html
   <!-- Format -->
   <a href="https://full-url.com">Link Text</a>
   ```

### Link Inventory
Current external links to update:
- Get Started button: `https://doorgaze.curatedspot.com/`
- Explore Smart Solutions button (hero section)
- Get Started Now button (call-to-action section)

## Linking Privacy and Terms Pages

### Adding Privacy and Terms Links
Located in the footer section:
```html
<!-- Before -->
<ul class="space-y-2 text-sm">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>

<!-- After -->
<ul class="space-y-2 text-sm">
    <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Creating Policy Pages
1. Create two new files in your root directory:
   - `privacy.html`
   - `terms.html`

2. Ensure consistent styling by copying the header and footer from `index.html`

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Verify that section IDs match the href attributes
   - Check for typos in IDs
   - Ensure sections have unique IDs

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify Tailwind breakpoint classes are correct
   - Test on different screen sizes

3. **Style Inconsistencies**
   - Maintain consistent color classes (e.g., `text-blue-600`)
   - Keep spacing consistent using similar padding/margin classes
   - Follow existing patterns for hover states and transitions

### Need Help?
For additional support:
- Check [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Review HTML basics on [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML)
- Contact support at: theintrovertedmarketer@protonmail.com

Remember to test all changes in multiple browsers and screen sizes before deploying to production.