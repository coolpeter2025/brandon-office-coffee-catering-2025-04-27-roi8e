# Delightful Bean Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Delightful Bean coffee catering landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

```html
<!-- Located at the top of the page -->
<a href="/" class="text-2xl font-bold text-gray-800">Delightful Bean</a>
```

To change the company name:
1. Locate this line in the header section
2. Replace "Delightful Bean" with your desired text
3. Maintain the existing classes to preserve styling

### Hero Section Text
The main headline and subheading are in the hero section:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight text-gray-900 mb-8">
    Brandon Office Coffee Catering
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 leading-relaxed">
    Brandon workplace coffee that inspires productivity
</p>
```

To modify:
1. Find these elements in the hero section
2. Update the text while keeping the HTML tags intact
3. The `text-4xl` class controls text size on mobile, while `md:text-5xl` and `lg:text-6xl` control tablet and desktop sizes

### Understanding Tailwind Classes
Common classes used throughout:
- `text-gray-600`: Sets text color to gray
- `mb-8`: Adds margin bottom (spacing)
- `py-24`: Adds padding top and bottom
- `container mx-auto`: Centers content and sets max width
- `rounded-lg`: Adds rounded corners
- `hover:scale-105`: Enlarges element on hover

## Managing Links

### Navigation Menu Links
The main navigation is in the header:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. Locate the `href` attribute
2. For internal page sections, use `#section-name`
3. For external links, use the full URL: `https://example.com`

### Call-to-Action Buttons
There are two main CTA buttons:

```html
<!-- Hero section button -->
<a href="https://www.delightfulbean.com/" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
    Get Started Today
</a>

<!-- Bottom CTA section button -->
<a href="https://www.delightfulbean.com/" class="inline-block bg-white text-blue-600 px-8 py-4 rounded-lg">
    Get Started Now
</a>
```

To update:
1. Replace the `href` value with your desired URL
2. Update the button text as needed
3. Maintain the existing classes for consistent styling

## Adding Privacy and Terms Pages

### Footer Links
Located in the footer section:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link to policy pages:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match the href values
   - Section IDs should not contain spaces
   - Example: `href="#features"` links to `<section id="features">`

2. **Responsive Design Issues**
   - Check mobile-specific classes (no prefix)
   - Tablet classes start with `md:`
   - Desktop classes start with `lg:`
   - Example: `text-4xl md:text-5xl lg:text-6xl`

3. **Missing Styles**
   - Verify the Tailwind CSS CDN link is present in the head section
   - Check for typos in class names
   - Ensure all classes are space-separated

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools to inspect elements
- Test all changes across different screen sizes
- Keep a backup of the original code before making changes

Remember to test all changes in multiple browsers and screen sizes to ensure consistency across devices.