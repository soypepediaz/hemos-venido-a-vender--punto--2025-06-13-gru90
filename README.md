# Landing Page Maintenance Guide

This guide will help you maintain and customize your landing page, even if you're new to web development. We'll focus on common updates while preserving the design and functionality.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your main navigation and logo. To update:

1. Change the logo text:
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    VENTAS  <!-- Replace this text -->
</a>
```

2. Update navigation menu items:
```html
<div class="hidden md:flex space-x-8">
    <!-- Modify these link texts as needed -->
    <a href="#features" class="hover:text-purple-400 transition-colors duration-300">Características</a>
    <a href="#benefits" class="hover:text-purple-400 transition-colors duration-300">Beneficios</a>
    <a href="#contact" class="hover:text-purple-400 transition-colors duration-300">Contacto</a>
</div>
```

### Hero Section
The main headline and subtitle can be updated here:
```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-extrabold mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    Hemos venido a vender. Punto.  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Que es lo que sabemos hacer.  <!-- Subtitle -->
</p>
```

### Features Section
Each feature card follows this structure:
```html
<div class="bg-gray-800 rounded-2xl p-8 transform hover:scale-105 transition-all duration-300 shadow-xl hover:shadow-2xl">
    <!-- Icon -->
    <h3 class="text-xl font-bold mb-4">Vender</h3>  <!-- Feature title -->
    <p class="text-gray-400">Maximizamos tus oportunidades...</p>  <!-- Feature description -->
</div>
```

### Styling Tips
- Font sizes use Tailwind's scale: `text-sm`, `text-base`, `text-lg`, `text-xl`, etc.
- Colors follow the pattern: `text-purple-400`, `bg-gray-800`, etc.
- Spacing uses multiples of 4: `p-4`, `m-8`, `space-x-8`, etc.

## Managing Links

### Internal Navigation Links
Current internal links point to page sections:
```html
<a href="#features">Características</a>
<a href="#benefits">Beneficios</a>
<a href="#contact">Contacto</a>
```

To update:
1. Ensure the `href` matches the section's `id` attribute
2. Example: `<section id="features">` pairs with `<a href="#features">`

### External Links
Current external links:
```html
<!-- Main CTA button -->
<a href="https://llcpasoapaso.com" class="inline-block px-8 py-4...">
    Empieza Ahora
</a>

<!-- Email link -->
<a href="mailto:llcpasoapaso@proton.me" class="text-lg text-purple-400...">
    llcpasoapaso@proton.me
</a>
```

To update external links:
1. Replace the `href` value with your new URL
2. Ensure URLs include `https://` for external sites
3. Use `mailto:` for email links

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer:
```html
<footer class="bg-gray-900 border-t border-gray-800 py-12">
    <div class="container mx-auto px-6">
        <div class="text-center text-gray-400">
            <p>&copy; 2024 Todos los derechos reservados</p>
            <!-- Add these lines below the copyright notice -->
            <div class="mt-4 space-x-4">
                <a href="/privacy.html" class="hover:text-purple-400 transition-colors duration-300">Privacidad</a>
                <a href="/terms.html" class="hover:text-purple-400 transition-colors duration-300">Términos</a>
            </div>
        </div>
    </div>
</footer>
```

### Creating Policy Pages
1. Create new files named `privacy.html` and `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Verify section `id` attributes match link `href` values
   - Check for typos in both the link and section ID
   - Ensure IDs are unique across the page

2. **Responsive Design Issues**
   - Keep responsive classes (`md:`, `lg:`) when updating styles
   - Test on multiple screen sizes after changes
   - Don't remove `container` and `mx-auto` classes

3. **Styling Problems**
   - Maintain the gradient classes for consistent design
   - Keep hover effects (`hover:`) for interactive elements
   - Don't remove transition classes for smooth animations

Remember to:
- Test all changes in multiple browsers
- Verify mobile responsiveness
- Keep backups before making significant changes
- Maintain consistent spacing and formatting

For additional help, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Alpine.js Documentation](https://alpinejs.dev/docs)