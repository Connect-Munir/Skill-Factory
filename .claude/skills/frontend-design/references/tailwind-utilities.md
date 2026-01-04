# Tailwind CSS Utilities Reference

Common Tailwind patterns and utilities for minimalistic web applications.

## Layout Utilities

### Flexbox Patterns

```html
<!-- Center content -->
<div class="flex items-center justify-center">

<!-- Space between items -->
<div class="flex items-center justify-between">

<!-- Stack vertically -->
<div class="flex flex-col">

<!-- Inline with gap -->
<div class="flex items-center gap-3">

<!-- Wrap items -->
<div class="flex flex-wrap gap-4">

<!-- Push item to end -->
<div class="flex items-center">
  <span>Left</span>
  <span class="ml-auto">Right</span>
</div>
```

### Grid Patterns

```html
<!-- Responsive columns -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">

<!-- Equal columns -->
<div class="grid grid-cols-3 gap-4">

<!-- Auto-fit columns (min 250px) -->
<div class="grid grid-cols-[repeat(auto-fit,minmax(250px,1fr))] gap-6">

<!-- Sidebar layout -->
<div class="grid grid-cols-[240px_1fr] gap-6">

<!-- Two columns with different ratios -->
<div class="grid grid-cols-[2fr_1fr] gap-6">
```

### Container Patterns

```html
<!-- Centered container with max-width -->
<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">

<!-- Full height page -->
<div class="min-h-screen">

<!-- Sticky footer layout -->
<div class="min-h-screen flex flex-col">
  <header>...</header>
  <main class="flex-1">...</main>
  <footer>...</footer>
</div>
```

### Positioning

```html
<!-- Sticky header -->
<header class="sticky top-0 z-50">

<!-- Fixed bottom bar -->
<div class="fixed bottom-0 left-0 right-0">

<!-- Absolute positioning -->
<div class="relative">
  <div class="absolute top-0 right-0">
  <div class="absolute inset-0"> <!-- Full coverage -->
  <div class="absolute -top-2 -right-2"> <!-- Overlap -->
</div>

<!-- Center absolute element -->
<div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2">
```

## Spacing

### Consistent Spacing Scale

```html
<!-- 4px increments -->
p-1    → 4px
p-2    → 8px
p-3    → 12px
p-4    → 16px
p-5    → 20px
p-6    → 24px
p-8    → 32px
p-10   → 40px
p-12   → 48px
p-16   → 64px
p-20   → 80px
p-24   → 96px
```

### Common Spacing Patterns

```html
<!-- Card padding -->
<div class="p-6">

<!-- Section padding -->
<section class="py-16 md:py-24">

<!-- Tight inline spacing -->
<div class="px-3 py-1.5">

<!-- Button spacing -->
<button class="px-4 py-2">

<!-- Form spacing -->
<form class="space-y-6">

<!-- List spacing -->
<ul class="space-y-2">

<!-- Inline item spacing -->
<div class="space-x-4">
```

## Typography

### Text Sizing

```html
text-xs    → 12px
text-sm    → 14px
text-base  → 16px
text-lg    → 18px
text-xl    → 20px
text-2xl   → 24px
text-3xl   → 30px
text-4xl   → 36px
text-5xl   → 48px
```

### Common Typography Patterns

```html
<!-- Page title -->
<h1 class="text-3xl font-bold text-slate-900 dark:text-white">

<!-- Section header -->
<h2 class="text-2xl font-semibold text-slate-900 dark:text-white">

<!-- Card title -->
<h3 class="text-lg font-semibold text-slate-900 dark:text-white">

<!-- Body text -->
<p class="text-base text-slate-600 leading-relaxed dark:text-slate-300">

<!-- Secondary text -->
<p class="text-sm text-slate-500 dark:text-slate-400">

<!-- Caption/label -->
<span class="text-xs text-slate-400 uppercase tracking-wide">

<!-- Link -->
<a class="text-blue-600 hover:text-blue-700 hover:underline">

<!-- Truncate text -->
<p class="truncate">

<!-- Line clamp -->
<p class="line-clamp-2">
```

### Font Weight

```html
font-normal    → 400
font-medium    → 500
font-semibold  → 600
font-bold      → 700
```

## Colors

### Semantic Color Usage

```html
<!-- Primary text -->
text-slate-900 dark:text-white

<!-- Secondary text -->
text-slate-600 dark:text-slate-300

<!-- Muted text -->
text-slate-500 dark:text-slate-400

<!-- Disabled text -->
text-slate-400 dark:text-slate-500

<!-- Background layers -->
bg-white dark:bg-slate-900              <!-- Base -->
bg-slate-50 dark:bg-slate-800           <!-- Surface -->
bg-slate-100 dark:bg-slate-700          <!-- Elevated -->

<!-- Borders -->
border-slate-200 dark:border-slate-700

<!-- Hover states -->
hover:bg-slate-100 dark:hover:bg-slate-800
```

### Status Colors

```html
<!-- Success -->
text-green-600 bg-green-50 border-green-200

<!-- Warning -->
text-amber-600 bg-amber-50 border-amber-200

<!-- Error -->
text-red-600 bg-red-50 border-red-200

<!-- Info -->
text-blue-600 bg-blue-50 border-blue-200
```

## Borders & Shadows

### Border Radius

```html
rounded-sm     → 2px
rounded        → 4px
rounded-md     → 6px
rounded-lg     → 8px
rounded-xl     → 12px
rounded-2xl    → 16px
rounded-full   → 9999px
```

### Common Border Patterns

```html
<!-- Card border -->
<div class="border border-slate-200 dark:border-slate-700 rounded-xl">

<!-- Divider -->
<hr class="border-slate-200 dark:border-slate-700">

<!-- Input border -->
<input class="border border-slate-300 focus:border-blue-500 rounded-lg">

<!-- Focus ring -->
<button class="focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2">
```

### Shadow Scale

```html
shadow-sm      → Subtle elevation
shadow         → Default card shadow
shadow-md      → Medium elevation
shadow-lg      → High elevation (modals)
shadow-xl      → Highest elevation
shadow-none    → Remove shadow
```

## Transitions & Animations

### Common Transitions

```html
<!-- Color transition -->
<button class="transition-colors">

<!-- All properties -->
<div class="transition-all">

<!-- Transform transition -->
<div class="transition-transform">

<!-- Opacity transition -->
<div class="transition-opacity">

<!-- Custom duration -->
<div class="transition-all duration-200">
<div class="transition-all duration-300">
```

### Built-in Animations

```html
<!-- Spin (for loaders) -->
<svg class="animate-spin">

<!-- Pulse (for skeletons) -->
<div class="animate-pulse">

<!-- Bounce -->
<div class="animate-bounce">

<!-- Ping (for notifications) -->
<span class="animate-ping">
```

### Hover & Focus States

```html
<!-- Button hover -->
<button class="bg-blue-600 hover:bg-blue-700 transition-colors">

<!-- Card hover -->
<div class="hover:shadow-md hover:border-slate-300 transition-all">

<!-- Scale on hover -->
<div class="hover:scale-105 transition-transform">

<!-- Opacity on hover -->
<div class="opacity-0 group-hover:opacity-100 transition-opacity">
```

## Responsive Design

### Breakpoints

```html
sm:    → 640px
md:    → 768px
lg:    → 1024px
xl:    → 1280px
2xl:   → 1536px
```

### Common Responsive Patterns

```html
<!-- Responsive columns -->
<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4">

<!-- Responsive padding -->
<section class="px-4 sm:px-6 lg:px-8">

<!-- Responsive text -->
<h1 class="text-2xl sm:text-3xl lg:text-4xl">

<!-- Hide/show on breakpoints -->
<div class="hidden md:block">     <!-- Hidden on mobile -->
<div class="block md:hidden">     <!-- Only on mobile -->

<!-- Responsive flex direction -->
<div class="flex flex-col md:flex-row">

<!-- Responsive spacing -->
<div class="space-y-4 md:space-y-0 md:space-x-4">
```

## Dark Mode

### Pattern for Dark Mode

```html
<!-- Background -->
<div class="bg-white dark:bg-slate-900">

<!-- Text -->
<p class="text-slate-900 dark:text-white">
<p class="text-slate-600 dark:text-slate-300">

<!-- Borders -->
<div class="border-slate-200 dark:border-slate-700">

<!-- Hover states -->
<button class="hover:bg-slate-100 dark:hover:bg-slate-800">
```

### Dark Mode Toggle Setup

```html
<!-- In tailwind.config.js -->
module.exports = {
  darkMode: 'class',
  // ...
}

<!-- Toggle class on html element -->
<html class="dark">
```

## Interactive States

### Focus States

```html
<!-- Button focus -->
<button class="focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2">

<!-- Input focus -->
<input class="focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent">

<!-- Link focus -->
<a class="focus:outline-none focus-visible:ring-2 focus-visible:ring-blue-500">
```

### Disabled States

```html
<button class="disabled:opacity-50 disabled:cursor-not-allowed disabled:pointer-events-none">

<input class="disabled:bg-slate-100 disabled:text-slate-400 disabled:cursor-not-allowed">
```

### Group Hover

```html
<div class="group">
  <div class="group-hover:visible">
  <div class="group-hover:opacity-100">
  <div class="group-hover:translate-x-1">
</div>
```

## Utility Combinations

### Card Component

```html
<div class="p-6 bg-white rounded-xl border border-slate-200 shadow-sm hover:shadow-md transition-shadow dark:bg-slate-800 dark:border-slate-700">
```

### Button Primary

```html
<button class="inline-flex items-center justify-center px-4 py-2 text-sm font-medium text-white bg-blue-600 rounded-lg hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2 transition-colors disabled:opacity-50 disabled:pointer-events-none">
```

### Input Field

```html
<input class="block w-full px-3 py-2 text-slate-900 bg-white border border-slate-300 rounded-lg placeholder-slate-400 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent dark:bg-slate-800 dark:border-slate-600 dark:text-white dark:placeholder-slate-500">
```

### Badge

```html
<span class="inline-flex items-center px-2.5 py-0.5 rounded-full text-xs font-medium bg-blue-100 text-blue-800 dark:bg-blue-900/30 dark:text-blue-300">
```

### Avatar

```html
<div class="w-10 h-10 rounded-full bg-slate-200 flex items-center justify-center text-slate-600 font-medium dark:bg-slate-700 dark:text-slate-300">
```

### Dropdown Menu

```html
<div class="absolute right-0 mt-2 w-48 bg-white rounded-lg shadow-lg border border-slate-200 py-1 z-50 dark:bg-slate-800 dark:border-slate-700">
  <a class="block px-4 py-2 text-sm text-slate-700 hover:bg-slate-100 dark:text-slate-300 dark:hover:bg-slate-700">
```

### Modal Overlay

```html
<div class="fixed inset-0 bg-black/50 backdrop-blur-sm flex items-center justify-center z-50">
  <div class="bg-white rounded-xl shadow-xl max-w-md w-full mx-4 dark:bg-slate-800">
```

## Accessibility Utilities

### Screen Reader Only

```html
<span class="sr-only">Description for screen readers</span>
```

### Skip Link

```html
<a href="#main" class="sr-only focus:not-sr-only focus:absolute focus:top-4 focus:left-4 focus:z-50 focus:px-4 focus:py-2 focus:bg-white focus:text-blue-600 focus:rounded-lg">
  Skip to main content
</a>
```

### Focus Visible

```html
<!-- Only show focus ring on keyboard navigation -->
<button class="focus:outline-none focus-visible:ring-2 focus-visible:ring-blue-500">
```
