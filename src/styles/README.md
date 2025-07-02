# HR Consulting Design System

A comprehensive CSS/SCSS design system based on the HR consulting website design, featuring a warm color palette with browns and orange accents, clean typography, and modern component patterns.

## Overview

This design system provides:

- **Design Tokens**: Colors, spacing, typography scales
- **Utility Classes**: Layout, spacing, typography utilities
- **Base Styles**: CSS reset and foundational styles
- **Component Classes**: Pre-built HR-specific components

## Color Palette

### Primary Colors (Brown/Chocolate)

- **Primary**: `#6b4423` (Dark brown for headers, buttons)
- **Primary Light**: `#a67c56` (Medium brown)
- **Primary Dark**: `#4a2e16` (Darkest brown)

### Secondary Colors (Orange/Coral)

- **Secondary**: `#ff6b35` (Orange accent from clothing)
- **Secondary Light**: `#ff7a4d` (Light orange)
- **Secondary Dark**: `#f04b1a` (Dark orange)

### Usage Examples

```css
/* Using CSS custom properties */
.primary-bg { background-color: var(--color-primary); }
.accent-text { color: var(--color-secondary); }

/* Using utility classes */
.bg-primary { background-color: var(--color-primary); }
.text-brand-secondary { color: var(--color-secondary); }
```

```scss
/* Using SCSS variables */
.primary-bg { background-color: $color-primary; }
.accent-text { color: $color-secondary; }
```

## Typography

### Font Families

- **Primary**: Inter (clean, modern sans-serif)
- **Secondary**: Roboto (alternative sans-serif)
- **Display**: Playfair Display (elegant serif for large headings)

### Font Scales

- **xs**: 0.75rem (12px)
- **sm**: 0.875rem (14px)
- **base**: 1rem (16px)
- **lg**: 1.125rem (18px)
- **xl**: 1.25rem (20px)
- **2xl**: 1.5rem (24px)
- **3xl**: 1.875rem (30px)
- **4xl**: 2.25rem (36px)
- **5xl**: 3rem (48px)

### Usage Examples

```css
/* Semantic typography classes */
.hero-title { /* Large display heading */ }
.section-title { /* Section headings */ }
.card-title { /* Card headings */ }
.button-text { /* Button text styling */ }

/* Utility classes */
.text-2xl { font-size: var(--font-size-2xl); }
.font-semibold { font-weight: var(--font-weight-semibold); }
.leading-relaxed { line-height: var(--line-height-relaxed); }
```

## Spacing System

Based on a 4px grid system:

- **0**: 0
- **1**: 0.25rem (4px)
- **2**: 0.5rem (8px)
- **3**: 0.75rem (12px)
- **4**: 1rem (16px)
- **6**: 1.5rem (24px)
- **8**: 2rem (32px)
- **12**: 3rem (48px)
- **16**: 4rem (64px)
- **20**: 5rem (80px)
- **24**: 6rem (96px)

### Usage Examples

```css
/* Margin utilities */
.m-4 { margin: var(--spacing-4); }
.mt-6 { margin-top: var(--spacing-6); }
.mx-auto { margin-left: auto; margin-right: auto; }

/* Padding utilities */
.p-6 { padding: var(--spacing-6); }
.px-4 { padding-left: var(--spacing-4); padding-right: var(--spacing-4); }
.py-8 { padding-top: var(--spacing-8); padding-bottom: var(--spacing-8); }

/* Semantic spacing */
.section-spacing { padding-top: var(--section-spacing-md); padding-bottom: var(--section-spacing-md); }
.card-spacing { padding: var(--card-padding); }
```

## Layout Utilities

### Display

```css
.flex { display: flex; }
.grid { display: grid; }
.block { display: block; }
.hidden { display: none; }
```

### Flexbox

```css
.flex-col { flex-direction: column; }
.items-center { align-items: center; }
.justify-between { justify-content: space-between; }
.gap-md { gap: var(--spacing-4); }
```

### Grid

```css
.grid-cols-3 { grid-template-columns: repeat(3, minmax(0, 1fr)); }
.col-span-2 { grid-column: span 2 / span 2; }
```

### Container

```css
.container {
  width: 100%;
  max-width: 1200px;
  margin-left: auto;
  margin-right: auto;
  padding-left: var(--container-padding-md);
  padding-right: var(--container-padding-md);
}
```

## Components

### Buttons

```html
<button class="btn btn-primary">Primary Button</button>
<button class="btn btn-secondary">Secondary Button</button>
<button class="btn btn-outline">Outline Button</button>
```

### Cards

```html
<div class="card">
  <div class="card-icon">📊</div>
  <h3 class="card-title">Service Title</h3>
  <p class="card-text">Service description goes here.</p>
  <button class="btn btn-primary">Learn More</button>
</div>
```

### Navigation

```html
<nav class="navbar">
  <div class="container">
    <a href="/" class="navbar-brand">LuxHR</a>
    <ul class="navbar-nav">
      <li><a href="/services">Services</a></li>
      <li><a href="/about">About</a></li>
      <li><a href="/contact">Contact</a></li>
    </ul>
  </div>
</nav>
```

### Hero Section

```html
<section class="hero">
  <div class="container">
    <div class="hero-content">
      <div>
        <h1 class="hero-title">Leading with heart, building with strategy</h1>
        <p class="hero-subtitle">Transform your HR operations and achieve your business goals.</p>
        <button class="btn btn-secondary">Work With Us</button>
      </div>
      <div class="hero-image">
        <img src="hero-image.jpg" alt="HR Consulting">
      </div>
    </div>
  </div>
</section>
```

## File Structure

```
src/styles/
├── tokens/
│   ├── colors.css/scss       # Color design tokens
│   ├── spacing.css/scss      # Spacing design tokens
│   └── typography.css/scss   # Typography design tokens
├── utilities/
│   ├── layout.css/scss       # Layout utility classes
│   ├── spacing.css/scss      # Spacing utility classes
│   └── typography.css/scss   # Typography utility classes
├── base.css/scss            # CSS reset and base styles
├── style.css/scss           # Main stylesheet (imports everything)
└── README.md               # This documentation
```

## Usage

### CSS Version

```html
<link rel="stylesheet" href="./styles/style.css">
```

### SCSS Version

```scss
@use './styles/style' as *;
```

## Responsive Design

The system includes mobile-first responsive utilities and breakpoints:

- **sm**: 640px and up
- **md**: 768px and up
- **lg**: 1024px and up
- **xl**: 1280px and up

Example responsive usage:

```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-md">
  <!-- Content adapts from 1 column on mobile to 3 columns on large screens -->
</div>
```

## Accessibility

The design system includes:

- Sufficient color contrast ratios (WCAG AA compliant)
- Focus states for interactive elements
- Semantic HTML structure
- Screen reader friendly utilities (`.sr-only`)

## Best Practices

1. **Use design tokens**: Always use CSS custom properties or SCSS variables instead of hardcoded values
2. **Leverage utility classes**: Combine utility classes for rapid prototyping
3. **Follow the spacing system**: Stick to the 4px grid system for consistent spacing
4. **Use semantic classes**: Use component classes like `.hero-title` for specific use cases
5. **Mobile-first**: Design for mobile screens first, then enhance for larger screens

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Contributing

When adding new components or utilities:

1. Follow the existing naming conventions
2. Use design tokens instead of hardcoded values
3. Include both CSS and SCSS versions
4. Update this documentation
5. Test across different screen sizes
