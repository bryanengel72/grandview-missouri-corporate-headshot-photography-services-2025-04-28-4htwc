# Landing Page Maintenance Guide
## For 101Headshots Corporate Photography Website

This guide provides detailed instructions for maintaining and customizing the 101Headshots landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Main Sections Overview
The landing page consists of these key sections:
- Header (Navigation)
- Hero Section
- Features Section
- Contact Section
- Footer

### Updating Text Content

#### Header/Navigation
```html
<!-- Located in the nav section -->
<a href="/" class="text-2xl font-bold">101Headshots</a>
```
To update the company name, modify the text between the `<a>` tags.

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">
    Grandview, Missouri Corporate Headshot Photography Services
</h1>
```
To update the main headline:
1. Locate this `<h1>` tag in the hero section
2. Replace the text while keeping the HTML tags intact
3. Maintain the existing classes to preserve styling

#### Features Section
Each feature card follows this structure:
```html
<div class="bg-gray-800 rounded-2xl p-8">
    <h3 class="text-xl font-semibold mb-4">Market Edge</h3>
    <p class="text-gray-400">Stand out from the competition...</p>
</div>
```
To update feature cards:
1. Locate the feature section (`id="features"`)
2. Find each card within the grid
3. Update the `<h3>` title and `<p>` description text

### Modifying Tailwind CSS Classes

#### Understanding Responsive Classes
The site uses these breakpoints:
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
- Layout: `container`, `mx-auto`, `px-6`, `py-4`
- Flexbox: `flex`, `items-center`, `justify-between`
- Colors: `bg-gray-900`, `text-gray-100`, `from-purple-500`
- Typography: `text-2xl`, `font-bold`, `text-center`

## Fixing Broken Links

### Current Link Structure
```html
<!-- Navigation Links -->
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>

<!-- Call-to-Action Links -->
<a href="https://www.101headshots.com">Book Now</a>

<!-- Email Links -->
<a href="mailto:bryan@101headshots.com">bryan@101headshots.com</a>
```

### Updating Links
1. Internal Links (Same Page):
   ```html
   <!-- Format: -->
   <a href="#section-id">Section Name</a>
   ```
   - Must match the `id` of the target section
   - Always start with `#`

2. External Links:
   ```html
   <!-- Format: -->
   <a href="https://full-website-url.com">Link Text</a>
   ```
   - Always include `https://` or `http://`
   - Test links after updating

3. Email Links:
   ```html
   <!-- Format: -->
   <a href="mailto:your-email@domain.com">your-email@domain.com</a>
   ```

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer's Quick Links section:

```html
<div>
    <h3 class="text-xl font-bold mb-4">Quick Links</h3>
    <ul class="space-y-2">
        <!-- Existing links -->
        <li><a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a></li>
        <!-- Add new links -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating Policy Pages
1. Create new files:
   - `privacy.html`
   - `terms.html`
2. Use the same header and footer as `index.html`
3. Maintain consistent styling using Tailwind classes

## Troubleshooting

### Common Issues and Solutions

1. Broken Internal Links
   - Check that section `id` attributes match link `href` values
   - Ensure no spaces in `id` names

2. Responsive Design Issues
   - Verify Tailwind responsive classes (`md:`, `lg:`)
   - Test on different screen sizes

3. Styling Inconsistencies
   - Compare classes with existing elements
   - Maintain color scheme using provided gradient classes

### Need Help?
If you encounter issues:
1. Check the Tailwind CSS documentation
2. Verify HTML syntax
3. Test in multiple browsers
4. Ensure all files are in the correct directory

Remember to always backup your files before making changes, and test thoroughly after modifications.