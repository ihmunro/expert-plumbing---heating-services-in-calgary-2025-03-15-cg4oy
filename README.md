# Calgary Plumbing Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Calgary Plumbing landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company logo and navigation menu:

```html
<a href="/" class="text-2xl font-bold text-blue-600">Calgary<span class="text-gray-800">Plumbing</span></a>
```

To modify:
1. Change company name: Replace "Calgary" and "Plumbing"
2. Adjust color: Replace `text-blue-600` with other Tailwind colors (e.g., `text-red-600`)
3. Modify size: Change `text-2xl` to `text-3xl` for larger text

### Hero Section
Located at the top of the page with main heading and CTA buttons:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Expert Plumbing & Heating Services in Calgary
</h1>
```

To customize:
1. Update heading text between the `<h1>` tags
2. Adjust responsive sizes:
   - Mobile: `text-4xl`
   - Tablet: `md:text-5xl`
   - Desktop: `lg:text-6xl`

### Features Section
Contains three feature cards with icons:

```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <i class='bx bx-user text-3xl text-blue-600'></i>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-4">User Friendly</h3>
    <p class="text-gray-600">Simple booking process...</p>
</div>
```

To modify:
1. Change icon: Replace `bx-user` with other Boxicons classes
2. Update heading: Modify text in `<h3>` tags
3. Update description: Change text in `<p>` tags
4. Adjust spacing: Modify `p-8` padding or `mb-6` margin values

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#services" class="text-gray-600 hover:text-blue-600">Services</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600">FAQ</a>
    <a href="https://plumbers.com" class="bg-blue-600 text-white">Contact Us</a>
</div>
```

To update:
1. Internal links: Change `href="#section-name"`
2. External links: Replace `https://plumbers.com` with your actual URL
3. Ensure section IDs match link references

### Footer Links
Located at the bottom of the page:

```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Home</a></li>
    <li><a href="#services" class="hover:text-white transition-colors duration-300">Services</a></li>
    <!-- More links -->
</ul>
```

To fix:
1. Replace `href="#"` with actual page URLs
2. Update social media links in the Follow Us section
3. Ensure consistency with navigation menu links

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the Quick Links section:

```html
<ul class="space-y-2">
    <!-- Existing links -->
    <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Creating New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Copy header and footer from `index.html`
3. Add content between header and footer
4. Maintain consistent styling using Tailwind classes

## Troubleshooting

### Common Issues

1. **Broken Responsive Design**
   - Check for missing responsive classes (`md:`, `lg:`)
   - Verify container class is present: `container mx-auto`

2. **Missing Icons**
   - Ensure Boxicons CSS is properly linked
   - Check icon class names for typos

3. **Layout Problems**
   - Verify grid classes are correct (`grid-cols-1 md:grid-cols-3`)
   - Check for proper spacing classes (`space-x-8`, `gap-12`)

### Best Practices

1. Always test changes across different screen sizes
2. Maintain consistent color schemes using Tailwind classes
3. Keep spacing consistent using Tailwind's spacing scale
4. Test all links after updates
5. Validate HTML structure after modifications

For additional support or questions, contact the development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).