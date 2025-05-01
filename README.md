# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Best Websites Paris landing page. Follow these steps carefully to make updates while preserving the page's functionality and design.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<div class="text-2xl font-bold text-blue-600">
    Best Websites Paris  <!-- Replace this text -->
</div>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Update text here -->
    <a href="#benefits">Benefits</a>  <!-- Update text here -->
    <a href="#faq">FAQ</a>           <!-- Update text here -->
    <a href="#contact">Contact</a>    <!-- Update text here -->
</div>
```

### Hero Section
To modify the main headline and subtext:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 tracking-tight">
    Custom Websites For Your Business  <!-- Replace main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 leading-relaxed">
    Professional web development services...  <!-- Replace subheading -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this page:

- Text sizes: `text-xl`, `text-2xl`, `text-4xl`
- Colors: `text-blue-600`, `text-gray-900`
- Spacing: `px-6`, `py-4`, `mb-6`
- Responsive prefixes: `md:`, `lg:`

Example of modifying a button:
```html
<!-- Original button -->
<a href="https://sigmaseo.io" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">

<!-- To make button larger -->
<a href="https://sigmaseo.io" class="inline-block bg-blue-600 text-white px-10 py-5 rounded-lg">
```

## Managing Links

### Navigation Menu Links
Current internal links that need verification:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update these links:
1. Ensure section IDs match exactly:
```html
<section id="features"> <!-- ID must match href -->
```

### External Links
Current external links requiring updates:
```html
<!-- CTA Button -->
<a href="https://sigmaseo.io">Get Started Today</a>

<!-- Footer Social Media -->
<a href="#"><i class="fab fa-twitter"></i></a>
<a href="#"><i class="fab fa-linkedin"></i></a>
<a href="#"><i class="fab fa-facebook"></i></a>
```

To update:
1. Replace `#` with actual social media URLs
2. Update `https://sigmaseo.io` with your desired landing page

## Adding Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h3 class="text-xl font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Maintaining Consistent Styling
When creating privacy.html and terms.html:
1. Copy the header and footer from index.html
2. Use the same Tailwind CSS classes for consistency
3. Example structure:
```html
<!-- privacy.html or terms.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Copy head section from index.html -->
</head>
<body class="font-sans antialiased bg-white text-gray-900">
    <!-- Copy header section -->
    
    <!-- Add your privacy/terms content here -->
    <section class="pt-32 pb-24">
        <div class="container mx-auto px-6">
            <h1 class="text-4xl font-bold mb-8">Privacy Policy</h1>
            <!-- Add your content -->
        </div>
    </section>
    
    <!-- Copy footer section -->
</body>
</html>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Check that section IDs exactly match href attributes
   - IDs are case-sensitive
   - Remove any spaces in IDs

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Test on multiple screen sizes
   - Keep the viewport meta tag in place

3. **Icon Problems**
   - Ensure Font Awesome CDN link remains in the head section
   - Check that icon class names are correct (e.g., `fa-twitter`)

For additional help, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Font Awesome Icons](https://fontawesome.com/icons)

Remember to always test changes in multiple browsers and screen sizes before deploying to production.