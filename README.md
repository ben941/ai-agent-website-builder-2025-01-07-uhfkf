# AI Website Builder Landing Page - Maintenance Guide

This guide will help you maintain and customize the AI Website Builder landing page. Follow these instructions carefully to make updates while preserving the design and functionality.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header -->
<a href="#" class="text-xl font-bold bg-gradient-to-r from-blue-500 to-purple-600 bg-clip-text text-transparent">BWB</a>
```
- Replace "BWB" with your desired logo text
- Keep the classes to maintain the gradient effect

2. **Navigation Menu Items:**
```html
<a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
```
- Update the text between `<a>` tags
- Maintain the classes for proper styling and hover effects

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold bg-gradient-to-r from-blue-500 to-purple-600 bg-clip-text text-transparent mb-6">AI Agent Website Builder</h1>
<p class="text-xl md:text-2xl text-gray-400 mb-8">Best AI Website Builder</p>
```
- Update the heading and subheading text
- The classes control responsive text sizes:
  - `text-4xl`: base size
  - `md:text-5xl`: medium screens
  - `lg:text-6xl`: large screens

### Features Section
To modify feature cards:
```html
<div class="bg-gray-800 rounded-2xl p-8 hover:shadow-xl hover:shadow-blue-500/10 transition-all duration-300 transform hover:scale-105">
    <h3 class="text-xl font-semibold mb-4">No Code Required</h3>
    <p class="text-gray-400">Build your website without writing a single line of code.</p>
</div>
```
- Update the heading (`<h3>`) and description text
- Keep all classes to maintain hover effects and styling

## Fixing Broken Links

### Navigation Menu Links
Current links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="https://bwb.com">Get Started</a>
```
To update:
1. Internal links (starting with #) connect to section IDs
2. External links (https://) should be updated to your actual domain
3. Replace "https://bwb.com" with your actual website URL

### Call-to-Action Buttons
Find and update all CTA buttons:
```html
<a href="https://bwb.com" class="inline-block bg-gradient-to-r...">Start Building Now</a>
```
- Replace "https://bwb.com" with your actual signup or registration page URL
- Keep all classes to maintain button styling

## Linking Privacy and Terms Pages

### Footer Legal Links
Locate the legal section in the footer:
```html
<div>
    <h3 class="text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues:

1. **Broken Gradients**
If gradient text disappears:
- Ensure all gradient classes remain intact:
```html
bg-gradient-to-r from-blue-500 to-purple-600 bg-clip-text text-transparent
```

2. **Responsive Issues**
If mobile layout breaks:
- Check that responsive classes (md: and lg: prefixes) are present
- Verify the viewport meta tag exists in the head:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

3. **Missing Hover Effects**
If hover animations don't work:
- Ensure these classes are present on interactive elements:
```html
hover:shadow-lg hover:shadow-blue-500/25 transition-all duration-300 transform hover:scale-105
```

### Need Help?
- Always test changes in multiple browsers
- Use browser developer tools (F12) to inspect elements
- Make one change at a time and test
- Keep a backup of the original HTML file

Remember to maintain the responsive design by keeping all Tailwind CSS classes intact when making changes. If you're unsure about a modification, test it on both mobile and desktop views before finalizing.