# PolicyPals Landing Page - Maintenance Guide

This guide will help you maintain and customize the PolicyPals landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions to make updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To modify:

1. **Logo Text**:
```html
<a href="/" class="text-2xl font-bold text-blue-500">PolicyPals</a>
```
- Replace "PolicyPals" with your desired text
- Adjust size using `text-2xl` (options: text-sm, text-lg, text-3xl, etc.)
- Change color using `text-blue-500` (options: text-red-500, text-green-500, etc.)

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-8 bg-gradient-to-r from-blue-400 to-blue-600 bg-clip-text text-transparent">
    Policy Pals Find You The Friendliest Insurance Policies
</h1>
```
- Replace the headline text between the `<h1>` tags
- The gradient effect uses `from-blue-400 to-blue-600` - modify colors as needed
- Responsive text sizes are controlled by `text-4xl md:text-5xl lg:text-6xl`

### Features Section
Each feature card follows this structure:
```html
<div class="bg-gray-900 rounded-xl p-8 transform hover:scale-105 transition-all duration-300">
    <div class="text-blue-500 mb-4">
        <i class="fas fa-user-check text-3xl"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Personalised Policy Matching</h3>
    <p class="text-gray-400">Your feature description here</p>
</div>
```
To modify:
1. Change icon: Replace `fa-user-check` with any [Font Awesome](https://fontawesome.com/icons) icon
2. Update heading: Modify text in `<h3>` tag
3. Update description: Modify text in `<p>` tag

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="https://PolicyPals.Co.Uk">Get Started</a>
</div>
```

To update:
1. Internal links (starting with #) point to section IDs on the page
2. External links (starting with http) point to other websites
3. Replace `href` values with your desired destinations

### Call-to-Action (CTA) Links
Located in hero and CTA sections:
```html
<a href="https://PolicyPals.Co.Uk" class="inline-block bg-blue-600 hover:bg-blue-700 text-white text-lg px-8 py-4 rounded-full">
    Find Your Perfect Policy
</a>
```
- Update `href` with your destination URL
- Modify button text between the `<a>` tags

## Adding Privacy and Terms Pages

### Footer Link Setup
Locate the Legal section in the footer:
```html
<div>
    <h4 class="text-xl font-bold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-blue-400">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-blue-400">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create new files:
   - Create `privacy.html` in your project folder
   - Create `terms.html` in your project folder

2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-blue-400">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-blue-400">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Links**
   - Check for typos in `href` attributes
   - Ensure linked files exist in the correct directory
   - Verify that section IDs match their corresponding links

2. **Styling Issues**
   - If Tailwind classes aren't working:
     - Check if Tailwind CSS CDN is properly loaded
     - Verify class names for typos
     - Use browser inspector to check if classes are being applied

3. **Responsive Design**
   - If mobile layout looks wrong:
     - Check `md:` and `lg:` prefixed classes
     - Test different screen sizes using browser developer tools
     - Verify the viewport meta tag is present

### Need Help?
- Check [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Use browser developer tools (F12) to inspect elements

Remember to always test changes across different devices and browsers before deploying to production.