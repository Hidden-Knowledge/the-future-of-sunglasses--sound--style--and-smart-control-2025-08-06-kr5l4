# SmartShades Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the SmartShades landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Legal Pages](#adding-legal-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu:

```html
<div class="flex-shrink-0">
    <a href="/" class="text-2xl font-bold">SmartShades</a>
</div>
```

To update the company name:
1. Locate this section at the top of the page
2. Replace "SmartShades" with your desired text
3. Maintain the existing classes to preserve styling

### Hero Section Text
The main headline and subtext can be found here:

```html
<h1 class="text-4xl md:text-6xl font-bold leading-tight mb-6">
    The Future Of Sunglasses: Sound, Style, and Smart Control
</h1>
<p class="text-xl md:text-2xl mb-8">
    Smart Audio Meets Stylish Shades. All Day. Hands-Free.
</p>
```

To modify:
1. Update the text between the `<h1>` tags for the main headline
2. Change the text between the `<p>` tags for the subheading
3. Keep the existing classes to maintain responsive design:
   - `text-4xl`: Large text on mobile
   - `md:text-6xl`: Larger text on medium screens
   - `mb-6`: Bottom margin spacing

### Tailwind CSS Class Guide
Common classes used throughout:
- Text sizes: `text-sm`, `text-lg`, `text-xl`, `text-2xl`
- Spacing: `p-8` (padding), `m-4` (margin), `mb-6` (margin-bottom)
- Colors: `text-black`, `text-white`, `bg-black`, `bg-white`
- Hover effects: `hover:bg-gray-800`, `hover:scale-105`

## Managing Links

### Navigation Menu Links
Current navigation links are located in two places:

Desktop menu:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900">FAQ</a>
</div>
```

Mobile menu:
```html
<div class="md:hidden" x-show="isOpen" @click.away="isOpen = false">
    <div class="px-2 pt-2 pb-3 space-y-1">
        <a href="#features" class="block px-3 py-2 text-gray-600">Features</a>
        <a href="#benefits" class="block px-3 py-2 text-gray-600">Benefits</a>
        <a href="#faq" class="block px-3 py-2 text-gray-600">FAQ</a>
    </div>
</div>
```

To update links:
1. Identify the section you want to link to
2. Update the `href` attribute with either:
   - Internal link: `#section-id`
   - External link: `https://full-url.com`
3. Update both desktop and mobile menus to match

### Buy Now Links
The "Buy Now" buttons currently point to a placeholder Stripe URL:
```html
<a href="https://buy.stripe.com" class="bg-black text-white px-6 py-2 rounded-full">
    Buy Now
</a>
```

To update:
1. Search for all instances of `https://buy.stripe.com`
2. Replace with your actual payment or product page URL
3. Test all buttons to ensure they work correctly

## Adding Legal Pages

### Footer Modification
Add privacy and terms links to the footer:

1. Locate the footer's Quick Links section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
    <ul class="space-y-2">
        <!-- Add new links here -->
        <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors">Privacy Policy</a></li>
        <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors">Terms of Service</a></li>
    </ul>
</div>
```

2. Ensure your privacy.html and terms.html files are:
   - Located in the root directory
   - Use consistent styling with the main page
   - Include navigation back to the main page

## Troubleshooting

Common issues and solutions:

### Responsive Design Issues
If elements don't look right on mobile:
1. Check for `md:` prefixed classes
2. Ensure both mobile and desktop menus are properly updated
3. Test at various screen sizes using browser dev tools

### Broken Links
If links aren't working:
1. Verify all `href` attributes are correct
2. For internal links (#features, etc.), ensure IDs exist in the HTML
3. Test external links in a new tab

### Style Conflicts
If new styles aren't applying:
1. Check for competing Tailwind classes
2. Ensure classes are in the correct order
3. Use browser inspector to identify overridden styles

Need more help? Contact support at [support@smartshades.co](mailto:support@smartshades.co)