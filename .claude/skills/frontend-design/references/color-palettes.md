# Web Application Color Palettes

Curated color palettes optimized for minimalistic web applications. Each palette includes light/dark mode variants and Tailwind CSS classes.

## Neutral Foundations

### Slate (Recommended Default)

Cool gray with subtle blue undertones. Professional and modern.

```css
/* Light Mode */
--bg-primary: #ffffff;
--bg-secondary: #f8fafc;      /* slate-50 */
--bg-tertiary: #f1f5f9;       /* slate-100 */
--border: #e2e8f0;            /* slate-200 */
--text-primary: #0f172a;      /* slate-900 */
--text-secondary: #475569;    /* slate-600 */
--text-muted: #94a3b8;        /* slate-400 */

/* Dark Mode */
--bg-primary: #0f172a;        /* slate-900 */
--bg-secondary: #1e293b;      /* slate-800 */
--bg-tertiary: #334155;       /* slate-700 */
--border: #334155;            /* slate-700 */
--text-primary: #f8fafc;      /* slate-50 */
--text-secondary: #cbd5e1;    /* slate-300 */
--text-muted: #64748b;        /* slate-500 */
```

**Tailwind Classes:**
```html
<!-- Light -->
<div class="bg-white text-slate-900">
<div class="bg-slate-50 text-slate-600">
<div class="border-slate-200">

<!-- Dark -->
<div class="dark:bg-slate-900 dark:text-slate-50">
<div class="dark:bg-slate-800 dark:text-slate-300">
<div class="dark:border-slate-700">
```

### Zinc (Neutral Gray)

Pure neutral gray. No undertones.

```css
/* Light Mode */
--bg-primary: #ffffff;
--bg-secondary: #fafafa;      /* zinc-50 */
--bg-tertiary: #f4f4f5;       /* zinc-100 */
--border: #e4e4e7;            /* zinc-200 */
--text-primary: #18181b;      /* zinc-900 */
--text-secondary: #52525b;    /* zinc-600 */
--text-muted: #a1a1aa;        /* zinc-400 */

/* Dark Mode */
--bg-primary: #18181b;        /* zinc-900 */
--bg-secondary: #27272a;      /* zinc-800 */
--bg-tertiary: #3f3f46;       /* zinc-700 */
--border: #3f3f46;            /* zinc-700 */
--text-primary: #fafafa;      /* zinc-50 */
--text-secondary: #d4d4d8;    /* zinc-300 */
--text-muted: #71717a;        /* zinc-500 */
```

### Stone (Warm Gray)

Warm gray with subtle brown undertones. Friendly and approachable.

```css
/* Light Mode */
--bg-primary: #ffffff;
--bg-secondary: #fafaf9;      /* stone-50 */
--bg-tertiary: #f5f5f4;       /* stone-100 */
--border: #e7e5e4;            /* stone-200 */
--text-primary: #1c1917;      /* stone-900 */
--text-secondary: #57534e;    /* stone-600 */
--text-muted: #a8a29e;        /* stone-400 */
```

## Primary Color Palettes

### Blue Professional

Classic, trustworthy. Great for business applications.

```css
--primary: #2563eb;           /* blue-600 */
--primary-hover: #1d4ed8;     /* blue-700 */
--primary-light: #dbeafe;     /* blue-100 */
--primary-muted: #93c5fd;     /* blue-300 */
```

**Tailwind:**
```html
<button class="bg-blue-600 hover:bg-blue-700 text-white">
<div class="bg-blue-50 text-blue-700 border-blue-200">
<span class="text-blue-600">
```

### Indigo Modern

Sophisticated, tech-forward. Great for SaaS products.

```css
--primary: #4f46e5;           /* indigo-600 */
--primary-hover: #4338ca;     /* indigo-700 */
--primary-light: #e0e7ff;     /* indigo-100 */
--primary-muted: #a5b4fc;     /* indigo-300 */
```

**Tailwind:**
```html
<button class="bg-indigo-600 hover:bg-indigo-700 text-white">
<div class="bg-indigo-50 text-indigo-700">
```

### Violet Creative

Creative, innovative. Great for design tools.

```css
--primary: #7c3aed;           /* violet-600 */
--primary-hover: #6d28d9;     /* violet-700 */
--primary-light: #ede9fe;     /* violet-100 */
--primary-muted: #c4b5fd;     /* violet-300 */
```

### Emerald Growth

Fresh, positive. Great for finance, health apps.

```css
--primary: #059669;           /* emerald-600 */
--primary-hover: #047857;     /* emerald-700 */
--primary-light: #d1fae5;     /* emerald-100 */
--primary-muted: #6ee7b7;     /* emerald-300 */
```

### Amber Warm

Energetic, optimistic. Great for creative, social apps.

```css
--primary: #d97706;           /* amber-600 */
--primary-hover: #b45309;     /* amber-700 */
--primary-light: #fef3c7;     /* amber-100 */
--primary-muted: #fcd34d;     /* amber-300 */
```

### Rose Accent

Bold, passionate. Great for lifestyle, entertainment.

```css
--primary: #e11d48;           /* rose-600 */
--primary-hover: #be123c;     /* rose-700 */
--primary-light: #ffe4e6;     /* rose-100 */
--primary-muted: #fda4af;     /* rose-300 */
```

## Status Colors

Standard semantic colors for states and feedback.

```css
/* Success */
--success: #16a34a;           /* green-600 */
--success-light: #dcfce7;     /* green-100 */
--success-text: #166534;      /* green-800 */

/* Warning */
--warning: #d97706;           /* amber-600 */
--warning-light: #fef3c7;     /* amber-100 */
--warning-text: #92400e;      /* amber-800 */

/* Error */
--error: #dc2626;             /* red-600 */
--error-light: #fee2e2;       /* red-100 */
--error-text: #991b1b;        /* red-800 */

/* Info */
--info: #0284c7;              /* sky-600 */
--info-light: #e0f2fe;        /* sky-100 */
--info-text: #075985;         /* sky-800 */
```

**Tailwind Status Components:**
```html
<!-- Success Alert -->
<div class="bg-green-50 border border-green-200 text-green-800 rounded-lg p-4">

<!-- Warning Alert -->
<div class="bg-amber-50 border border-amber-200 text-amber-800 rounded-lg p-4">

<!-- Error Alert -->
<div class="bg-red-50 border border-red-200 text-red-800 rounded-lg p-4">

<!-- Info Alert -->
<div class="bg-sky-50 border border-sky-200 text-sky-800 rounded-lg p-4">
```

## Complete Theme Examples

### Minimal Light

Clean, spacious, professional.

```css
:root {
  --bg: #ffffff;
  --surface: #f8fafc;
  --surface-elevated: #ffffff;
  --border: #e2e8f0;
  --text: #0f172a;
  --text-secondary: #475569;
  --text-muted: #94a3b8;
  --primary: #18181b;
  --primary-hover: #27272a;
  --accent: #2563eb;
}
```

### Minimal Dark

Modern, focused, easy on the eyes.

```css
:root {
  --bg: #09090b;
  --surface: #18181b;
  --surface-elevated: #27272a;
  --border: #27272a;
  --text: #fafafa;
  --text-secondary: #a1a1aa;
  --text-muted: #52525b;
  --primary: #fafafa;
  --primary-hover: #f4f4f5;
  --accent: #3b82f6;
}
```

### SaaS Dashboard

```css
:root {
  /* Background layers */
  --bg-app: #f1f5f9;
  --bg-card: #ffffff;
  --bg-sidebar: #1e293b;

  /* Text */
  --text-primary: #0f172a;
  --text-secondary: #475569;
  --text-inverse: #f8fafc;

  /* Primary */
  --primary: #6366f1;
  --primary-hover: #4f46e5;

  /* Accents for data */
  --chart-1: #6366f1;
  --chart-2: #22c55e;
  --chart-3: #f59e0b;
  --chart-4: #ef4444;
  --chart-5: #8b5cf6;
}
```

## Dark Mode Implementation

### CSS Variables Approach

```css
:root {
  --bg: #ffffff;
  --text: #0f172a;
}

[data-theme="dark"] {
  --bg: #0f172a;
  --text: #f8fafc;
}
```

### Tailwind Dark Mode

```html
<!-- Enable in tailwind.config.js: darkMode: 'class' -->

<html class="dark">
  <body class="bg-white dark:bg-slate-900 text-slate-900 dark:text-slate-50">
```

### System Preference Detection

```js
// Check system preference
const prefersDark = window.matchMedia('(prefers-color-scheme: dark)').matches;

// Listen for changes
window.matchMedia('(prefers-color-scheme: dark)')
  .addEventListener('change', e => {
    document.documentElement.classList.toggle('dark', e.matches);
  });
```

## Accessibility Color Contrast

### WCAG AA Compliant Pairs

| Background | Text | Ratio |
|------------|------|-------|
| white | slate-600 | 5.74:1 |
| white | slate-700 | 8.19:1 |
| white | slate-900 | 15.39:1 |
| slate-900 | slate-100 | 11.69:1 |
| slate-900 | slate-200 | 9.85:1 |
| slate-900 | white | 15.39:1 |
| blue-600 | white | 4.54:1 |
| emerald-600 | white | 4.52:1 |

### Testing Tools

- Chrome DevTools: Inspect > Color picker shows contrast ratio
- Figma: Stark plugin
- Online: WebAIM Contrast Checker

## Quick Reference

### Button Colors
```html
<!-- Primary -->
<button class="bg-blue-600 hover:bg-blue-700 text-white">

<!-- Secondary -->
<button class="bg-slate-100 hover:bg-slate-200 text-slate-700">

<!-- Danger -->
<button class="bg-red-600 hover:bg-red-700 text-white">

<!-- Ghost -->
<button class="text-slate-600 hover:bg-slate-100">
```

### Badge Colors
```html
<span class="bg-blue-100 text-blue-700">Blue</span>
<span class="bg-green-100 text-green-700">Green</span>
<span class="bg-amber-100 text-amber-700">Amber</span>
<span class="bg-red-100 text-red-700">Red</span>
<span class="bg-slate-100 text-slate-700">Gray</span>
```
