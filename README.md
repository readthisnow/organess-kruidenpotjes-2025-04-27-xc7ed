# Organess Landing Page Maintenance Guide

This guide will help you maintain and customize the Organess landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Organess <!-- Change this text to update the logo -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Kenmerken</a> <!-- Update these text labels -->
    <a href="#benefits">Voordelen</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
To modify the main headline and subtext:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    Koop Organess Kruidenpotjes Met Korting <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 max-w-3xl mx-auto">
    Nog maar enkele exemplaren beschikbaar! <!-- Subheading text -->
</p>
```

### Tailwind CSS Classes Explained
- `text-4xl`: Large text size (mobile)
- `md:text-5xl`: Larger text on medium screens
- `lg:text-6xl`: Largest text on large screens
- `mb-8`: Margin bottom spacing
- `bg-gradient-to-r`: Right-direction gradient
- `text-transparent`: Makes text transparent for gradient
- `max-w-3xl`: Maximum width constraint

## Managing Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#features">Kenmerken</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. The `#` symbol indicates an internal section link
2. Ensure the href matches the section's ID exactly
3. Example: `href="#features"` links to `<section id="features">`

### Call-to-Action Buttons
Current product link:
```html
<a href="https://amzn.to/3EGbl5G" class="inline-block bg-gradient-to-r from-purple-600 to-pink-600 px-8 py-4 rounded-full">
    Bekijk Aanbieding
</a>
```

To update:
1. Replace `https://amzn.to/3EGbl5G` with your new product link
2. Maintain the full URL including `https://`
3. Test the link before publishing

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-purple-400">
        <i class="fab fa-facebook text-2xl"></i>
    </a>
    <a href="#" class="text-gray-400 hover:text-purple-400">
        <i class="fab fa-instagram text-2xl"></i>
    </a>
</div>
```

To update:
1. Replace `#` with your social media profile URLs
2. Example: `href="https://facebook.com/your-page"`

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Replace the placeholder links in the footer:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="privacy.html" class="hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-purple-400 transition-colors duration-300">Terms & Conditions</a></li>
</ul>
```

### Step 3: Maintain Consistent Styling
Copy these classes to maintain consistent link styling:
```html
class="hover:text-purple-400 transition-colors duration-300"
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - Ensure no spaces in IDs
   - Example: `href="#features"` must match `id="features"`

2. **Responsive Design Issues**
   - Check mobile display using browser dev tools
   - Verify media query classes (md:, lg:) are correct
   - Common classes:
     - `md:` for medium screens (768px+)
     - `lg:` for large screens (1024px+)

3. **Gradient Text Not Showing**
   - Ensure all three classes are present:
     ```html
     bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent
     ```

4. **Social Icons Not Displaying**
   - Verify Font Awesome CSS is properly linked
   - Check icon class names against Font Awesome documentation
   - Ensure internet connectivity for CDN access

Remember to:
- Always test changes in multiple browsers
- Validate HTML using W3C Validator
- Back up files before making significant changes
- Test all links before publishing updates