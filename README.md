# Modern Landing Page - Maintenance Guide

This guide will help you maintain and customize the landing page, with specific instructions for updating content, fixing links, and adding policy pages.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**
```html
<!-- Find this line in the header section -->
<div class="text-2xl font-bold text-gray-800">Logo</div>
```
- Replace "Logo" with your company name
- Adjust size using `text-2xl` (options: `text-xl`, `text-3xl`, `text-4xl`)

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Home</a>
    <!-- Additional menu items -->
</div>
```
- Update text between `>` and `</a>` for each link
- Keep the classes intact to maintain hover effects

### Hero Section
Located at the top of the page with the main heading:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-8">
    Welcome to Our Modern Platform
</h1>
<p class="text-xl text-gray-600 mb-12 leading-relaxed">
    Transform your digital presence with our cutting-edge solutions.
</p>
```
- Update heading text between the `<h1>` tags
- Modify subtitle text in the `<p>` tag
- Keep responsive classes (`md:text-5xl lg:text-6xl`) to maintain mobile compatibility

### Feature Cards
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-bold text-gray-900 mb-4">Lightning Fast</h3>
    <p class="text-gray-600 leading-relaxed">Experience unparalleled speed...</p>
</div>
```
- Update heading text in `<h3>` tags
- Modify description in `<p>` tags
- Maintain the class structure for consistent styling

## Managing Links

### Navigation Menu Links
Current placeholder links:
```html
<a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Home</a>
```
To update:
1. Replace `#` with proper URLs:
   - Internal pages: `href="about.html"`
   - External links: `href="https://example.com"`
2. Keep all classes to maintain hover effects

### Footer Links
Located in the bottom section:
```html
<ul class="space-y-4">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Home</a></li>
    <!-- Additional footer links -->
</ul>
```
To update:
1. Replace `#` with actual URLs
2. Update text between `<a>` tags
3. Maintain the `hover:text-white` class for consistent styling

### Social Media Links
Found in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="hover:text-white transition-colors duration-300">
        <span class="sr-only">Twitter</span>
        <!-- SVG icon -->
    </a>
</div>
```
To update:
1. Replace `#` with social media profile URLs
2. Update `sr-only` text for accessibility
3. Keep SVG icons and styling classes

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links in the Quick Links section:
```html
<ul class="space-y-4">
    <!-- Existing links -->
    <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Creating New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Copy the header and footer from `index.html`
3. Add content between them
4. Maintain consistent styling using Tailwind classes

## Troubleshooting

### Common Issues

1. **Broken Styles**
- Verify Tailwind CSS link in header:
```html
<link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
```
- Check for typos in class names

2. **Responsive Issues**
- Keep responsive classes intact:
  - `md:` for tablet screens
  - `lg:` for desktop screens
- Test on different devices/screen sizes

3. **Link Problems**
- Ensure file paths are correct
- Check for proper URL formatting
- Verify files exist in specified locations

### Need Help?
- Double-check HTML syntax
- Maintain all original classes when updating
- Test all links after modifications
- View page in multiple browsers

Remember to always backup your files before making changes, and test your modifications in a development environment first.