# Delft Bouwmachine Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Delft Bouwmachine landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
```html
<header class="fixed w-full bg-white shadow-md z-50">
    <div class="flex-shrink-0">
        <h1 class="text-2xl font-bold text-blue-600">Delft Bouwmachine</h1>
    </div>
</header>
```
To update the company name:
1. Locate the `<h1>` tag in the header
2. Replace "Delft Bouwmachine" with your desired text
3. Keep the existing classes to maintain styling

### Hero Section
```html
<section id="hero" class="pt-32 pb-20 bg-gradient-to-r from-blue-50 to-blue-100">
    <h2 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
        LAATSTE KANS! De Beste Bouwmachines Nu Beschikbaar
    </h2>
</section>
```
To modify the hero section:
1. Find the `<h2>` tag within the hero section
2. Update the text while maintaining the following classes:
   - `text-4xl`: Base font size
   - `md:text-5xl`: Tablet screen size
   - `lg:text-6xl`: Desktop screen size

### Tailwind CSS Class Guide
Common classes used throughout:
- Font sizes: `text-xl`, `text-2xl`, `text-3xl`
- Colors: `text-blue-600`, `text-gray-600`, `bg-white`
- Spacing: `px-4`, `py-4`, `mb-6`, `mt-8`
- Responsive: `md:grid-cols-2`, `lg:grid-cols-3`

## Fixing Broken Links

### Navigation Menu Links
Current navigation links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600">Machines</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600">Voordelen</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600">Contact</a>
</div>
```

To update internal links:
1. Locate the `href` attribute
2. Ensure the `#` matches the `id` of the target section
3. Example: `href="#features"` links to `<section id="features">`

### External Links
Current external links:
```html
<a href="https://hansschuiling.nl" class="inline-block bg-blue-600">
    Direct Reserveren
</a>
```

To update external links:
1. Replace the `href` value with your desired URL
2. Ensure URLs include `https://` or `http://`
3. Test links after updating

## Linking Privacy and Terms Pages

### Footer Links Section
```html
<div>
    <h3 class="text-xl font-bold mb-4">Links</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-blue-400">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-blue-400">Terms & Conditions</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your project folder
2. Update the footer links:
```html
<li><a href="privacy.html" class="hover:text-blue-400">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400">Terms & Conditions</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section `id` attributes match link `href` values
   - Example: `href="#features"` must match `<section id="features">`

2. **Responsive Design Issues**
   - Verify responsive classes are present:
     ```html
     text-4xl md:text-5xl lg:text-6xl
     grid-cols-1 md:grid-cols-2 lg:grid-cols-3
     ```
   - Test on different screen sizes

3. **Missing Styles**
   - Ensure Tailwind CSS CDN is properly linked:
     ```html
     <script src="https://cdn.tailwindcss.com"></script>
     ```
   - Check for typos in class names

### Need Help?
- Double-check all changes against this original HTML
- Test all links after updating
- View the page in different browsers
- Use browser developer tools (F12) to inspect elements

Remember to always backup your files before making changes, and test thoroughly after updates.