# Landing Page Maintenance Guide

This guide will help you maintain and customize your landing page. Follow these detailed instructions to make updates while preserving the design and functionality.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
```html
<a href="#" class="text-2xl font-['Playfair_Display'] font-bold text-gray-900">Logo</a>
```
- Replace "Logo" with your company name
- Keep the font styles intact to maintain design consistency

#### Hero Section
```html
<h1 class="font-['Playfair_Display'] text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">Lorem ipsum dolor</h1>
<p class="text-xl text-gray-600 max-w-2xl mx-auto mb-10">Lorem ipsum dolor</p>
```
- Replace both "Lorem ipsum dolor" instances with your actual heading and subheading
- Maintain similar length to preserve layout

#### Features and Benefits Sections
Look for these repeated elements:
```html
<h3 class="text-xl font-semibold text-gray-900 mb-4">Lorem ipsum dolor</h3>
<p class="text-gray-600">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
```
- Update each feature/benefit title and description
- Keep descriptions concise (1-2 sentences)

### Tailwind CSS Classes Explained

#### Responsive Design Classes
- `md:` prefix: Applies styles on medium screens (768px+)
- `lg:` prefix: Applies styles on large screens (1024px+)
- Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
This makes text larger as screen size increases

#### Common Class Patterns
1. Spacing:
   - `px-4`: Horizontal padding
   - `py-24`: Vertical padding
   - `mb-6`: Bottom margin

2. Colors:
   - `text-gray-900`: Dark text
   - `text-gray-600`: Medium text
   - `bg-white`: White background

3. Layout:
   - `max-w-7xl`: Maximum width container
   - `mx-auto`: Center horizontally
   - `grid grid-cols-1 md:grid-cols-2`: Responsive grid layout

## Fixing Broken Links

### Navigation Menu Links
Current navigation structure:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact Us</a>
```

To update:
1. Internal links (starting with #) connect to section IDs
2. For external links, replace # with full URL:
```html
<a href="https://yourwebsite.com/page">Link Text</a>
```

### Contact Section Link
```html
<a href="mailto:Lorem ipsum dolor">Lorem ipsum dolor</a>
```
Replace with your email:
```html
<a href="mailto:your.email@domain.com">your.email@domain.com</a>
```

## Linking Privacy and Terms Pages

### Footer Links Section
Current structure:
```html
<li><a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Terms of Service</a></li>
```

To link to policy pages:
1. Create privacy.html and terms.html in your root directory
2. Update href attributes:
```html
<li><a href="privacy.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. Broken Layout
- Check for missing closing tags
- Verify Tailwind CSS classes are spelled correctly
- Ensure responsive classes use correct breakpoint prefixes

2. Missing Styles
- Confirm the Tailwind CDN link is working:
```html
<script src="https://cdn.tailwindcss.com"></script>
```

3. Font Issues
- Verify Google Fonts link is present and working:
```html
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
```

### Need Help?
- Check class names against [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Inspect elements using browser developer tools (Right-click > Inspect)
- Test responsive layouts using browser device emulation

Remember to always test your changes across different screen sizes and browsers to ensure consistency.