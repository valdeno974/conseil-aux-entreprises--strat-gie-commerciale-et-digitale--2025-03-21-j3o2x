# Valdeno Landing Page Maintenance Guide

This guide will help you maintain and customize the Valdeno Consulting landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Legal Pages](#adding-legal-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<div class="text-2xl font-bold text-gray-800">Valdeno</div>
```
Simply replace "Valdeno" with your desired text.

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-gray-900">Services</a>
    <a href="#avantages" class="text-gray-600 hover:text-gray-900">Avantages</a>
</div>
```
Change the text between `<a>` tags to update menu items.

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight text-gray-900 mb-6">
    Conseil aux entreprises
    <span class="block text-blue-600 mt-2">stratégie commerciale et digitale</span>
</h1>
```
- Update main heading by replacing "Conseil aux entreprises"
- Change subheading by modifying text within `<span>` tags
- Adjust text size using Tailwind classes:
  - `text-4xl`: Large screens
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Small screens

### Services Section
Each service card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl">
    <h3 class="text-xl font-bold mb-4">Stratégie commerciale</h3>
    <p class="text-gray-600">Optimisez votre approche commerciale...</p>
</div>
```
To modify:
1. Change service title in `<h3>` tags
2. Update description in `<p>` tags
3. Adjust styling using Tailwind classes:
   - `p-8`: Padding
   - `shadow-lg`: Shadow effect
   - `rounded-2xl`: Border radius

## Managing Links

### Navigation Links
Current navigation links are:
```html
<a href="#services">Services</a>
<a href="#avantages">Avantages</a>
<a href="#contact">Nous contacter</a>
```
To update:
1. Change internal links (starting with #) to match section IDs
2. For external links, replace with full URL:
```html
<a href="https://your-website.com/page">Link Text</a>
```

### Contact Links
Located in the contact section:
```html
<a href="mailto:contact@valdeno-consulting.com">contact@valdeno-consulting.com</a>
<a href="https://contact.valdeno.re/">Prendre rendez-vous</a>
```
Update by:
1. Changing email address in both the `href` and display text
2. Replacing booking link with your scheduling system URL

## Adding Legal Pages

### Footer Legal Links
Current placeholder links:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white">Mentions légales</a></li>
    <li><a href="#" class="hover:text-white">Politique de confidentialité</a></li>
</ul>
```

To add proper legal page links:
1. Create your legal pages (e.g., `mentions-legales.html`, `politique-confidentialite.html`)
2. Update the links:
```html
<li><a href="mentions-legales.html" class="hover:text-white">Mentions légales</a></li>
<li><a href="politique-confidentialite.html" class="hover:text-white">Politique de confidentialité</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check that all `href` attributes have correct paths
   - Verify that linked files exist in the correct directory
   - Test all links after updating

2. **Responsive Design**
   - If elements look wrong on mobile:
     - Check for `md:` prefixed classes
     - Ensure the viewport meta tag is present
     - Test on different screen sizes

3. **Styling Problems**
   - If Tailwind styles aren't applying:
     - Verify the Tailwind CSS CDN link is working
     - Check for typos in class names
     - Ensure classes are space-separated

### Need Help?
- Refer to [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Test changes using browser developer tools (F12)
- Make backup copies before significant changes

Remember to test all changes across different devices and browsers to ensure consistency.