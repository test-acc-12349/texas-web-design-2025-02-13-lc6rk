# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. It's written for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Company Name/Logo**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-blue-600">Texas Web Design</a>
```
- Replace "Texas Web Design" with your company name
- Adjust text size by changing `text-2xl` to `text-xl` (smaller) or `text-3xl` (larger)

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600">Benefits</a>
    <!-- Add or modify menu items here -->
</div>
```
- Change menu text by replacing words like "Features" or "Benefits"
- Keep the `href` attributes matching your section IDs

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Best Websites In Texas</h1>
<p class="text-xl text-gray-600 mb-8">Professional web design services tailored for Texas businesses</p>
```
- Update heading text between `<h1>` tags
- Modify subtitle text in the `<p>` tag
- Responsive text sizes are controlled by `text-4xl md:text-5xl lg:text-6xl`
  - `text-4xl`: Mobile devices
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Feature Cards
Each feature card follows this structure:
```html
<div class="p-8 bg-white rounded-2xl shadow-lg hover:shadow-xl">
    <h3 class="text-xl font-semibold mb-4">Free Hosting</h3>
    <p class="text-gray-600">Professional hosting included with every website package</p>
</div>
```
To modify:
1. Change the title between `<h3>` tags
2. Update description in the `<p>` tag
3. Maintain the existing classes for consistent styling

## Managing Links

### External Links
Current placeholder links that need updating:
```html
<!-- Header "Get Started" button -->
<a href="https://twd.com" class="hidden md:inline-block px-6 py-2 bg-blue-600">

<!-- Hero section buttons -->
<a href="https://twd.com" class="px-8 py-4 bg-blue-600">
```
To update:
1. Replace `https://twd.com` with your actual website URL
2. Ensure all URLs include `https://` or `http://`
3. Test links after updating

### Internal Links
Section links in navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
These link to page sections using IDs. Ensure:
1. Each linked section has a matching `id` attribute
2. IDs are unique and lowercase
3. No spaces in IDs (use hyphens if needed)

## Adding Privacy and Terms Pages

### Footer Links
Current placeholder privacy/terms links:
```html
<div>
    <h4 class="text-white text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create `privacy.html` and `terms.html` in your website directory
2. Update the links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Links**
   - Check for typos in URLs
   - Verify file names match exactly (case-sensitive)
   - Ensure files are in the correct directory

2. **Styling Issues**
   - Don't remove classes unless you're sure of their purpose
   - Keep the `class="..."` attribute format intact
   - Maintain spacing between class names

3. **Responsive Design**
   - Classes starting with `md:` affect tablets and up
   - Classes starting with `lg:` affect desktop sizes
   - Test changes at different screen sizes

4. **Text Not Updating**
   - Look for content between opening and closing tags
   - Example: `<p>Update this text</p>`
   - Save files after making changes
   - Refresh browser to see updates

Remember to:
- Always backup files before making changes
- Test all modifications in a browser
- Check your site on different devices
- Validate links before publishing updates

Need more help? Contact your web development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).