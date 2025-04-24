# Albert Park Accounting Landing Page - Maintenance Guide

Welcome to the maintenance guide for the Albert Park Accounting landing page. This document will help you make common updates and modifications to the website, even if you're new to web development.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. Company Name:
```html
<div class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Albert Park <!-- Change company name here -->
</div>
```

2. Navigation Menu Items:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a> <!-- Update menu text here -->
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    Your financial success is our bottom line <!-- Change headline here -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Expert accounting solutions tailored to drive your business forward <!-- Change subheading here -->
</p>
```

### Tailwind CSS Tips for Beginners
- Text sizes use classes like `text-sm`, `text-xl`, `text-2xl`
- Colors use format `text-gray-100`, `bg-gray-900`
- Spacing uses `m` (margin) or `p` (padding) with numbers: `p-4`, `mb-8`
- Responsive classes start with screen sizes: `md:text-6xl`

## Managing Links

### Navigation Menu Links
Current internal links point to page sections:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```

To update these:
1. Find the section ID you want to link to
2. Add a `#` before the ID in the href
3. Example: `<a href="#new-section">New Section</a>`

### Call-to-Action Links
Update the main CTA buttons:
```html
<!-- Hero section button -->
<a href="https://theaccountants.com" class="inline-block bg-gradient-to-r from-purple-600 to-pink-600...">
    Transform Your Finances
</a>

<!-- Contact section buttons -->
<a href="mailto:support@example.com">support@example.com</a>
<a href="https://theaccountants.com">Get Started Now</a>
```

Replace `https://theaccountants.com` with your actual website URL and `support@example.com` with your contact email.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your website directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate the Legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Replace the `href="#"` with:
- `href="privacy.html"` for Privacy Policy
- `href="terms.html"` for Terms of Service

### Step 3: Maintain Consistent Styling
Copy these classes to maintain consistent link styling:
```html
class="text-gray-400 hover:text-white transition-colors duration-300"
```

## Troubleshooting

### Common Issues and Solutions

1. **Links Not Working**
   - Check if the file names match exactly (including case)
   - Ensure files are in the same directory
   - Verify the `href` attributes start with `#` for internal section links

2. **Styling Issues**
   - Make sure Tailwind CSS is properly loaded
   - Check for typos in class names
   - Verify responsive classes use correct breakpoints (`sm:`, `md:`, `lg:`)

3. **Text Not Visible**
   - Check if text color contrasts with background
   - Verify gradient text has `bg-clip-text` and `text-transparent`

### Getting Help
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all HTML tags are properly closed
3. Ensure all required CSS classes are present
4. Compare your changes against the original code

Remember to always backup your files before making changes!