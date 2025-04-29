# Landing Page Maintenance Guide

This guide will help you maintain and customize the WebAgency landing page. Follow these detailed instructions to make common updates while preserving the design integrity.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

1. Change company name:
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-blue-600">WebAgency</a>
```
Simply replace "WebAgency" with your company name.

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Best Web Agency In Sydney</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-8">Grow your business with clicks</p>
```

To modify:
1. Replace the h1 text between the tags
2. Update the subheading in the p tag
3. The classes like `text-4xl` control text size:
   - `text-4xl`: Large on mobile
   - `md:text-5xl`: Larger on medium screens
   - `lg:text-6xl`: Largest on large screens

### Features Section
Each feature card follows this structure:
```html
<div class="p-8 rounded-2xl bg-white shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-lg flex items-center justify-center mb-6">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Easy to Use</h3>
    <p class="text-gray-600">Intuitive interface designed for seamless user experience...</p>
</div>
```

To update:
1. Locate the feature you want to change
2. Modify the h3 text for the feature title
3. Update the p tag content for the description
4. Keep the existing classes to maintain styling

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. The `href="#features"` format links to sections within the page
2. For external links, use complete URLs: `href="https://example.com"`
3. For internal pages, use relative paths: `href="/about.html"`

### Call-to-Action (CTA) Links
Current CTA links point to "https://fixrr.online". To update:
```html
<!-- Find these lines -->
<a href="https://fixrr.online" class="inline-block px-8 py-4 bg-blue-600 text-white...">
```
Replace the URL with your desired destination.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
1. Create two new files:
   - `privacy.html`
   - `terms.html`

### Step 2: Update Footer Links
Locate this section in the footer:
```html
<div>
    <h3 class="text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Update the links:
```html
<li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Check that files are in the correct directory
   - Verify file names match exactly (case-sensitive)

2. **Styling Problems**
   - Don't remove Tailwind CSS classes unless you're replacing them
   - Keep responsive classes (md:, lg:) to maintain mobile compatibility
   - Test on multiple screen sizes after making changes

3. **Layout Issues**
   - Maintain the container structure:
     ```html
     <div class="container mx-auto px-6">
         <!-- Content here -->
     </div>
     ```
   - Don't remove structural classes like `grid`, `flex`, or spacing utilities

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Test all changes in multiple browsers
- Keep a backup of the original code before making changes

Remember to always test your changes thoroughly before pushing to production!