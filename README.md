# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text (TWD)**
```html
<!-- Find this line in the header -->
<div class="text-2xl font-bold text-blue-600">TWD</div>
```
- Replace "TWD" with your desired text
- Adjust size using `text-2xl` (options: text-sm, text-base, text-lg, text-2xl, text-3xl)
- Change color using `text-blue-600` (options: text-[color]-[shade])

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Best Websites In Texas</p>
```
- Update headings and subheadings by changing the text within these tags
- Responsive text sizes are defined using `md:` and `lg:` prefixes
- Spacing is controlled by `mb-` classes (margin-bottom)

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 mb-4"><i class="fas fa-server text-3xl"></i></div>
    <h3 class="text-xl font-semibold mb-4">Free Hosting</h3>
    <p class="text-gray-600">Premium hosting included with every website package.</p>
</div>
```
To modify:
1. Change icon: Update `fa-server` to any [Font Awesome](https://fontawesome.com/icons) icon name
2. Update heading: Replace text within `<h3>` tags
3. Update description: Modify text within `<p>` tags

## Fixing Broken Links

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

To update:
1. Internal links (same page): Keep the `#` prefix followed by the section ID
2. External links: Replace `href="#section-name"` with full URL (e.g., `href="https://example.com"`)
3. Replace all instances of `https://twd.com` with your actual domain

### Call-to-Action Buttons
Located in multiple sections:
```html
<a href="https://twd.com" class="inline-block px-8 py-4 bg-blue-600 text-white rounded-full">Start Your Project</a>
```
- Update `href` attribute with your desired URL
- Maintain the same class structure for consistent styling

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the Quick Links section:
```html
<ul class="space-y-2">
    <li><a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a></li>
    <!-- Add these new lines -->
    <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

## Troubleshooting

### Common Issues

1. **Broken Responsive Design**
   - Check for missing `md:` or `lg:` prefixes in Tailwind classes
   - Ensure container classes remain intact: `container mx-auto px-6`

2. **Missing Icons**
   - Verify Font Awesome CDN link in header is present
   - Check icon class names match exactly with Font Awesome names

3. **Inconsistent Spacing**
   - Use `mb-` (margin-bottom) and `py-` (padding-vertical) classes consistently
   - Maintain spacing hierarchy: sections use `py-24`, elements use `mb-4`, `mb-8`, etc.

### CSS Class Reference

Common Tailwind classes used in this landing page:
- `container mx-auto`: Centers content and sets max-width
- `px-6`: Horizontal padding
- `py-24`: Vertical padding (top and bottom)
- `text-gray-600`: Text color
- `hover:text-blue-600`: Hover state text color
- `transition-colors`: Smooth color transitions
- `duration-300`: Transition duration in milliseconds

Remember to:
- Test all links after updating
- Maintain consistent spacing and styling
- Preview changes on multiple screen sizes
- Keep backup copies of working code

For additional help, consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or reach out to your development team.