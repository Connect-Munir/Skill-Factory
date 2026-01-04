---
name: frontend-design
description: Expert frontend web application designer specializing in minimalistic, clean UI patterns. Creates modern, accessible interfaces using HTML, CSS, Tailwind CSS, and JavaScript. Focuses on simplicity, readability, and excellent user experience with minimalistic SVG icons.
---

# Frontend Design Skill

Expert in creating minimalistic, modern web application interfaces with clean design patterns. Specializes in HTML, CSS, Tailwind CSS, and JavaScript.

## Design Philosophy

### Core Principles

1. **Minimalism First**: Every element must earn its place. Remove visual clutter ruthlessly.
2. **Function Over Form**: Design serves the user's goals, not aesthetic preferences.
3. **Consistency**: Uniform spacing, typography, and component behavior throughout.
4. **Accessibility**: WCAG 2.1 AA compliance is mandatory, not optional.
5. **Performance**: Lightweight assets, optimized rendering, minimal dependencies.

### The Minimalist Approach

- **Negative space is a feature**: Generous whitespace improves readability
- **Limited color palette**: 3-5 colors maximum
- **Subtle interactions**: Micro-animations, not flashy effects
- **Content hierarchy**: Size and weight guide attention
- **Flat design**: Avoid gradients, shadows unless absolutely necessary

## Typography System

### Font Selection

**Recommended System Font Stack** (Zero network requests):
```css
font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, sans-serif;
```

**Recommended Display Fonts**:
- Inter (versatile, modern)
- Plus Jakarta Sans (elegant)
- DM Sans (geometric, clean)
- Outfit (friendly, readable)

**Recommended Monospace**:
- JetBrains Mono
- Fira Code
- SF Mono

### Typography Scale (8px base)

```
Display:    48px / 3rem    - Hero headings
H1:         36px / 2.25rem - Page titles
H2:         28px / 1.75rem - Section headers
H3:         22px / 1.375rem - Subsection headers
H4:         18px / 1.125rem - Card titles
Body:       16px / 1rem    - Primary content
Small:      14px / 0.875rem - Secondary text
Caption:    12px / 0.75rem - Labels, hints
```

### Tailwind Typography Classes

```html
<!-- Display -->
<h1 class="text-5xl font-bold tracking-tight">

<!-- Page Title -->
<h1 class="text-3xl font-semibold">

<!-- Section Header -->
<h2 class="text-2xl font-semibold">

<!-- Body Text -->
<p class="text-base text-gray-700 leading-relaxed">

<!-- Small/Secondary -->
<span class="text-sm text-gray-500">

<!-- Caption -->
<span class="text-xs text-gray-400">
```

## Color Strategy

### Semantic Color Tokens

```css
/* Light Mode */
--color-background: #ffffff;
--color-surface: #f8fafc;
--color-surface-elevated: #ffffff;
--color-border: #e2e8f0;
--color-text-primary: #0f172a;
--color-text-secondary: #475569;
--color-text-muted: #94a3b8;
--color-primary: #2563eb;
--color-primary-hover: #1d4ed8;
--color-success: #16a34a;
--color-warning: #d97706;
--color-error: #dc2626;

/* Dark Mode */
--color-background: #0f172a;
--color-surface: #1e293b;
--color-surface-elevated: #334155;
--color-border: #334155;
--color-text-primary: #f8fafc;
--color-text-secondary: #cbd5e1;
--color-text-muted: #64748b;
```

### Tailwind Color Usage

```html
<!-- Background layers -->
<div class="bg-white dark:bg-slate-900">           <!-- Base -->
<div class="bg-slate-50 dark:bg-slate-800">        <!-- Surface -->
<div class="bg-white dark:bg-slate-700">           <!-- Elevated -->

<!-- Text hierarchy -->
<h1 class="text-slate-900 dark:text-white">        <!-- Primary -->
<p class="text-slate-600 dark:text-slate-300">     <!-- Secondary -->
<span class="text-slate-400 dark:text-slate-500">  <!-- Muted -->

<!-- Borders -->
<div class="border border-slate-200 dark:border-slate-700">

<!-- Interactive -->
<button class="bg-blue-600 hover:bg-blue-700 text-white">
```

## Spacing System

### 8px Grid System

All spacing should be multiples of 8px for visual consistency.

```
4px  - 0.25rem (px-1)   - Tight spacing, icon gaps
8px  - 0.5rem  (px-2)   - Compact elements
12px - 0.75rem (px-3)   - Default inline spacing
16px - 1rem    (px-4)   - Component padding
24px - 1.5rem  (px-6)   - Section padding
32px - 2rem    (px-8)   - Large gaps
48px - 3rem    (px-12)  - Section margins
64px - 4rem    (px-16)  - Page sections
```

### Common Spacing Patterns

```html
<!-- Card padding -->
<div class="p-6">

<!-- Section spacing -->
<section class="py-16 md:py-24">

<!-- Stack spacing (vertical) -->
<div class="space-y-4">

<!-- Inline spacing (horizontal) -->
<div class="space-x-3">

<!-- Grid gaps -->
<div class="grid gap-6">
```

## Minimalistic SVG Icons

### Mobile Responsive Menu

### STEP 8: Responsive Design Rules

Ensure the landing page works perfectly on all devices:

### Icon Design Rules

1. **24x24px** base viewBox (scalable)
2. **Stroke-based** design (not filled)
3. **2px stroke width** for consistency
4. **Rounded caps and joins** for friendliness
5. **Single color** using currentColor

### Icon Wrapper Function (Vanilla JavaScript)

```javascript
function createIcon(paths, size = 24, className = "") {
  const svg = document.createElementNS("http://www.w3.org/2000/svg", "svg");
  svg.setAttribute("width", size);
  svg.setAttribute("height", size);
  svg.setAttribute("viewBox", "0 0 24 24");
  svg.setAttribute("fill", "none");
  svg.setAttribute("stroke", "currentColor");
  svg.setAttribute("stroke-width", "2");
  svg.setAttribute("stroke-linecap", "round");
  svg.setAttribute("stroke-linejoin", "round");
  if (className) svg.className = className;
  svg.innerHTML = paths;
  return svg;
}
```

### Tailwind Icon Sizing

```html
<svg class="w-4 h-4">   <!-- 16px - Inline/small -->
<svg class="w-5 h-5">   <!-- 20px - Buttons -->
<svg class="w-6 h-6">   <!-- 24px - Default -->
<svg class="w-8 h-8">   <!-- 32px - Feature icons -->
<svg class="w-12 h-12"> <!-- 48px - Hero icons -->
```

## Component Patterns

### Buttons

```html
<!-- Primary -->
<button class="inline-flex items-center justify-center px-4 py-2 text-sm font-medium text-white bg-blue-600 rounded-lg hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2 transition-colors">
  Button
</button>

<!-- Secondary -->
<button class="inline-flex items-center justify-center px-4 py-2 text-sm font-medium text-slate-700 bg-slate-100 rounded-lg hover:bg-slate-200 focus:outline-none focus:ring-2 focus:ring-slate-500 focus:ring-offset-2 transition-colors dark:text-slate-200 dark:bg-slate-800 dark:hover:bg-slate-700">
  Button
</button>

<!-- Ghost -->
<button class="inline-flex items-center justify-center px-4 py-2 text-sm font-medium text-slate-600 hover:text-slate-900 hover:bg-slate-100 rounded-lg focus:outline-none focus:ring-2 focus:ring-slate-500 focus:ring-offset-2 transition-colors">
  Button
</button>

<!-- Icon Button -->
<button class="inline-flex items-center justify-center w-10 h-10 text-slate-600 hover:text-slate-900 hover:bg-slate-100 rounded-lg transition-colors">
  <svg class="w-5 h-5">...</svg>
</button>
```

### Cards

```html
<!-- Basic Card -->
<div class="p-6 bg-white rounded-xl border border-slate-200 dark:bg-slate-800 dark:border-slate-700">
  <h3 class="text-lg font-semibold text-slate-900 dark:text-white">Title</h3>
  <p class="mt-2 text-slate-600 dark:text-slate-300">Description</p>
</div>

<!-- Interactive Card -->
<div class="p-6 bg-white rounded-xl border border-slate-200 hover:border-slate-300 hover:shadow-sm transition-all cursor-pointer dark:bg-slate-800 dark:border-slate-700 dark:hover:border-slate-600">
  ...
</div>
```

### Inputs

```html
<!-- Text Input -->
<div>
  <label class="block text-sm font-medium text-slate-700 dark:text-slate-300">
    Label
  </label>
  <input
    type="text"
    class="mt-1 block w-full px-3 py-2 bg-white border border-slate-300 rounded-lg text-slate-900 placeholder-slate-400 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent dark:bg-slate-800 dark:border-slate-600 dark:text-white"
    placeholder="Placeholder"
  />
</div>

<!-- With Icon -->
<div class="relative">
  <div class="absolute inset-y-0 left-0 pl-3 flex items-center pointer-events-none">
    <svg class="w-5 h-5 text-slate-400">...</svg>
  </div>
  <input class="pl-10 ..." />
</div>
```

### Navigation

```html
<!-- Top Navigation -->
<nav class="sticky top-0 z-50 bg-white/80 backdrop-blur-lg border-b border-slate-200 dark:bg-slate-900/80 dark:border-slate-800">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex items-center justify-between h-16">
      <!-- Logo -->
      <div class="flex-shrink-0">
        <span class="text-xl font-bold text-slate-900 dark:text-white">Logo</span>
      </div>
      <!-- Links -->
      <div class="hidden md:flex items-center space-x-8">
        <a href="#" class="text-sm font-medium text-slate-600 hover:text-slate-900 dark:text-slate-300 dark:hover:text-white">Link</a>
      </div>
    </div>
  </div>
</nav>
```

## Layout Patterns

### Container

```html
<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
  <!-- Content -->
</div>
```

### Responsive Grid

```html
<!-- 3-column grid -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
  ...
</div>

<!-- 4-column grid -->
<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
  ...
</div>
```

### Sidebar Layout

```html
<div class="flex h-screen">
  <!-- Sidebar -->
  <aside class="hidden lg:flex lg:flex-col lg:w-64 lg:border-r lg:border-slate-200 lg:bg-slate-50 dark:lg:bg-slate-800 dark:lg:border-slate-700">
    ...
  </aside>
  <!-- Main content -->
  <main class="flex-1 overflow-y-auto">
    ...
  </main>
</div>
```

## Tailwind Configuration

```js
// tailwind.config.js
module.exports = {
  darkMode: 'class',
  content: [
    './src/**/*.{js,html}',
    './public/**/*.html',
    './*.html',
  ],
  theme: {
    extend: {
      fontFamily: {
        sans: ['Inter var', 'system-ui', 'sans-serif'],
      },
    },
  },
  plugins: [],
};
```

### Global Styles

```css
/* globals.css */
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer base {
  html {
    @apply scroll-smooth;
  }
  body {
    @apply antialiased;
  }
}

@layer components {
  .container {
    @apply max-w-7xl mx-auto px-4 sm:px-6 lg:px-8;
  }
}
```

## Accessibility Requirements

### Mandatory Practices

1. **Color contrast**: 4.5:1 for normal text, 3:1 for large text
2. **Focus indicators**: Visible focus rings on all interactive elements
3. **Keyboard navigation**: All interactions work with keyboard
4. **ARIA labels**: Proper labeling for screen readers
5. **Semantic HTML**: Use correct elements (button, nav, main, etc.)

### Focus States

```html
<button class="focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2">
```

### Skip Links

```html
<a href="#main-content" class="sr-only focus:not-sr-only focus:absolute focus:top-4 focus:left-4 focus:z-50 focus:px-4 focus:py-2 focus:bg-white focus:text-blue-600 focus:rounded-lg">
  Skip to main content
</a>
```

## Performance Guidelines

### Image Optimization

```html
<!-- Use modern image formats with fallbacks -->
<picture>
  <source srcset="hero.webp" type="image/webp">
  <source srcset="hero.jpg" type="image/jpeg">
  <img src="hero.jpg" alt="Hero image" loading="lazy" width="1200" height="600">
</picture>
```

### Font Loading

```html
<!-- Preload critical fonts -->
<link rel="preload" href="/fonts/inter.woff2" as="font" type="font/woff2" crossorigin>

<!-- Use font-display for better performance -->
<style>
  @font-face {
    font-family: 'Inter';
    src: url('/fonts/inter.woff2') format('woff2');
    font-display: swap;
  }
</style>
```

### Lazy Loading

```javascript
// Lazy load components when needed
const loadComponent = async () => {
  const module = await import('./HeavyComponent.js');
  return module.default;
};
```

## Quality Checklist

Before delivering, verify:

- [ ] **Responsive Design** - Works on mobile, tablet, and desktop
- [ ] **Dark Mode** - Fully implemented light/dark theme toggle
- [ ] **Animations** - Smooth entrance animations, hover effects, no layout shifts
- [ ] **Navigation** - Sticky navigation with scroll effect and mobile menu
- [ ] **Typography** - Consistent, distinctive fonts loaded properly
- [ ] **Colors & Contrast** - Cohesive color palette with CSS variables, meets WCAG AA standards
- [ ] **Content** - Clear headline, features, testimonials, and CTAs
- [ ] **Accessibility** - Semantic HTML, ARIA labels, keyboard navigation, focus states
- [ ] **Images** - Optimized images with proper alt text
- [ ] **Forms** - Proper labels, loading states, and error handling
- [ ] **Performance** - Optimized images, fonts, animations, and async operations
- [ ] **CTAs** - Clear, compelling calls-to-action throughout


## Common Mistakes to Avoid

1. **Too many colors** - Stick to 3-5 colors max
2. **Inconsistent spacing** - Use the 8px grid
3. **Missing dark mode** - Always implement both themes
4. **Heavy shadows/effects** - Keep it flat and minimal
5. **Tiny touch targets** - Minimum 44x44px for buttons
6. **Missing loading states** - Show feedback for async actions
7. **No error handling** - Display errors gracefully
8. **Overusing animations** - Subtle transitions only

## Reference Files

See `references/` for:
- `color-palettes.md`: Extended web app color schemes
- `icon-library.md`: Minimalistic SVG icon paths
- `component-patterns.md`: Reusable component code
- `tailwind-utilities.md`: Common Tailwind patterns
