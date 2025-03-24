# Lasius Web Services Landing Page - Maintenance Guide

This guide will help you maintain and customize the Lasius Web Services landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

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
<a href="/" class="text-2xl font-bold tracking-tight hover:text-indigo-400 transition-colors">
    Lasius Web  <!-- Change this text -->
</a>
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
Located at the top of the page, this section contains the main headline and subheading:

```html
<h1 class="text-4xl md:text-6xl font-bold leading-tight mb-6">
    Transform your online presence.<br>  <!-- Main headline -->
    <span class="text-indigo-400">Dominate your market.</span>  <!-- Colored subheading -->
</h1>
```

### Understanding Tailwind Classes
Common classes used throughout the page:

- Text sizes: `text-xl`, `text-2xl`, `text-4xl`
- Colors: `text-gray-100`, `text-indigo-400`, `bg-gray-900`
- Spacing: `px-6`, `py-4`, `mb-8`, `mt-12`
- Responsive design: `md:text-6xl`, `md:grid-cols-2`

To modify styles:
1. Find the element you want to change
2. Locate its class attribute
3. Add or modify Tailwind classes as needed

Example:
```html
<!-- Original -->
<p class="text-xl text-gray-400">

<!-- Making text larger and darker -->
<p class="text-2xl text-gray-300">
```

## Managing Links

### Navigation Links
The page uses both internal anchor links and external links:

1. **Internal Links (Scroll to Section):**
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
- Ensure the href matches the id of the target section
- Example: `href="#features"` scrolls to `<section id="features">`

2. **External Links:**
```html
<!-- Update this URL to your actual website -->
<a href="https://lasiuswebservices.com" class="hidden md:block px-6 py-2">
    Get Started
</a>
```

### Footer Links
The footer contains multiple link sections:

```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-8">
    <!-- Services Section -->
    <ul class="space-y-2 text-gray-400">
        <li><a href="#">SEO</a></li>  <!-- Add your service page URLs -->
        <li><a href="#">Paid Ads</a></li>
        <li><a href="#">Web Design</a></li>
    </ul>
</div>
```

To update links:
1. Locate the `<a>` tag
2. Replace the `#` with your actual URL
3. Maintain the existing classes for consistent styling

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate the Legal section in the footer:

```html
<div>
    <h4 class="font-bold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <!-- Update these href attributes -->
        <li><a href="privacy.html" class="hover:text-white transition-colors">Privacy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors">Terms</a></li>
    </ul>
</div>
```

### Step 3: Maintain Consistent Styling
When creating privacy.html and terms.html:
1. Copy the header and footer from index.html
2. Use the same Tailwind CSS classes
3. Maintain the same color scheme and styling

Example privacy page structure:
```html
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <!-- Copy head section from index.html -->
</head>
<body class="bg-gray-900 text-gray-100 font-sans antialiased">
    <!-- Copy header section -->
    
    <main class="container mx-auto px-6 py-24">
        <h1 class="text-4xl font-bold mb-8">Privacy Policy</h1>
        <!-- Add your privacy policy content here -->
    </main>

    <!-- Copy footer section -->
</body>
</html>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Verify that href values match section IDs exactly
   - Check for typos in both the href and id attributes
   - Ensure section IDs are unique

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify `md:` prefixed classes are working
   - Ensure viewport meta tag is present in head

3. **Animation Problems**
   - Confirm AOS script is loaded
   - Check data-aos attributes on elements
   - Verify AOS initialization in script section

For additional help:
- Consult [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Review [AOS Animation documentation](https://michalsnik.github.io/aos/)
- Test all changes in multiple browsers

Remember to always backup your files before making significant changes.