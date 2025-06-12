# Layout Utilities - SCSS file

A utility-first SCSS file designed to simplify the creation of responsive and flexible layouts.

## 📦 Features

- Utility-based classes for Flexbox, Grid, Spacing, and Positioning
- Responsive support with intuitive breakpoint naming
- Consistent spacing scale
- Easy-to-compose layout structures

---

## 🚀 Flexbox System

### Basic Flexbox

```html
<div class="flex">
  <div>Item 1</div>
  <div>Item 2</div>
</div>

<div class="flex flex-col">
  <div>Item 1</div>
  <div>Item 2</div>
</div>
```

### Flex Columns Grid

```html
<div class="flex-columns">
  <div class="col-6">Half width</div>
  <div class="col-3">Quarter width</div>
  <div class="col-3">Quarter width</div>
</div>

<div class="flex-columns">
  <div class="col-auto">Auto width</div>
  <div class="col-4">One third</div>
  <div class="col-8">Two thirds</div>
</div>
```

### Flexbox Alignment

```html
<div class="flex justify-between align-center">
  <div>Left</div>
  <div>Center</div>
  <div>Right</div>
</div>

<div class="flex justify-center align-center" style="height: 200px;">
  <div>Centered both ways</div>
</div>
```

---

## 🧱 Grid System

### Basic Grid

```html
<div class="grid grid-cols-3 gap-4">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
  <div>Item 4</div>
  <div>Item 5</div>
  <div>Item 6</div>
</div>
```

### Responsive Auto-fit Grid

```html
<div class="grid grid-cols-auto-fit-250 gap-6">
  <div>Card 1</div>
  <div>Card 2</div>
  <div>Card 3</div>
  <div>Card 4</div>
</div>
```

### Grid Spans

```html
<div class="grid grid-cols-6 gap-4">
  <div class="col-span-2">Spans 2 columns</div>
  <div class="col-span-4">Spans 4 columns</div>
  <div class="col-span-full">Full width</div>
</div>
```

---

## 📏 Spacing Utilities

### Margin

```html
<div class="mt-4 mb-8 mx-6">
  Top: 1rem, Bottom: 2rem, Horizontal: 1.5rem
</div>

<div class="m-0">No margin</div>
<div class="my-10">Vertical margin: 2.5rem</div>
```

### Padding

```html
<div class="p-4">All sides: 1rem</div>
<div class="px-6 py-3">Horizontal: 1.5rem, Vertical: 0.75rem</div>
<div class="pt-8 pb-4">Top: 2rem, Bottom: 1rem</div>
```

### Gap

```html
<div class="flex gap-8">
  <div>Item with 2rem gap</div>
  <div>Between items</div>
</div>

<div class="grid grid-cols-2 gap-x-4 gap-y-8">
  <div>Different horizontal</div>
  <div>And vertical gaps</div>
  <div>Item 3</div>
  <div>Item 4</div>
</div>
```

---

## 📐 Layout Utilities

### Width & Height

```html
<div class="w-full h-auto">Full width, auto height</div>
<div class="w-50 h-screen">Half width, full viewport height</div>
<div class="w-fit h-fit">Content-sized</div>
```

### Display

```html
<div class="block">Block element</div>
<span class="inline-block">Inline-block</span>
<div class="hidden">Hidden element</div>
```

### Positioning

```html
<div class="relative">
  <div class="absolute" style="top: 10px; right: 10px;">
    Absolute positioned
  </div>
</div>

<div class="sticky" style="top: 0;">Sticky header</div>
```

### Text Alignment

```html
<div class="text-center">Centered text</div>
<div class="text-right">Right aligned</div>
<div class="text-justify">Justified text content</div>
```

---

## 📱 Responsive Utilities

### Responsive Flexbox

```html
<div class="flex-columns">
  <div class="col-6 col-sm-12">Half on desktop, full on mobile</div>
  <div class="col-6 col-sm-12">Half on desktop, full on mobile</div>
</div>
```

### Responsive Display

```html
<div class="block md:hidden">Show on mobile only</div>
<div class="hidden md:block">Show on desktop only</div>
<div class="flex sm:grid">Flex on mobile, grid on larger screens</div>
```

---

## 🧩 Layout Examples

### Card Layout

```html
<div class="grid grid-cols-auto-fit-300 gap-6 p-6">
  <div class="p-4" style="border: 1px solid #ddd;">
    <h3 class="mt-0 mb-3">Card Title</h3>
    <p class="mb-4">Card content here</p>
    <div class="flex justify-between align-center">
      <button>Action</button>
      <span>$29</span>
    </div>
  </div>
</div>
```

### Header Layout

```html
<header class="flex justify-between align-center px-6 py-4">
  <div class="flex align-center gap-3">
    <img src="logo.png" alt="Logo" style="height: 40px;">
    <h1 class="m-0">Brand</h1>
  </div>
  <nav class="flex gap-6">
    <a href="#">Home</a>
    <a href="#">About</a>
    <a href="#">Contact</a>
  </nav>
</header>
```

### Dashboard Layout

```html
<div class="grid grid-cols-4 gap-6 p-6 h-screen">
  <aside class="col-span-1 p-4" style="background: #f5f5f5;">
    Sidebar
  </aside>
  <main class="col-span-3">
    <div class="grid grid-cols-2 gap-4 mb-6">
      <div class="p-4" style="border: 1px solid #ddd;">Widget 1</div>
      <div class="p-4" style="border: 1px solid #ddd;">Widget 2</div>
    </div>
    <div class="p-4" style="border: 1px solid #ddd;">
      Main content area
    </div>
  </main>
</div>
```

## 🛠️ Usage

To get started with Layout Utilities in your SCSS project:

### 1. Install

Copy or include the utility SCSS file in your project. You can organize it in your SCSS structure like:

```bash
src/
  styles/
    utilities/
      _layout-utils.scss
    main.scss
```

### 2. Import Utilities

Import the utility file into your main SCSS file:

```scss
// main.scss
@use 'utilities/layout-utils';
```

Make sure your build setup (like Sass, Vite, or Webpack) supports SCSS module syntax or adjust with `@import` if using the older syntax.

### 3. Apply Classes

Use the utility classes directly in your HTML to build layouts quickly:

```html
<section class="grid grid-cols-3 gap-6">
  <div class="col-span-2 p-4">Main Content</div>
  <aside class="col-span-1 p-4">Sidebar</aside>
</section>
```

### 4. Customize (Optional)

You can customize spacing scales, breakpoints, or add new utility classes by extending the SCSS partial.

```scss
// Example: Add a new spacing value
$spacing-scale: (
  0: 0,
  1: 0.25rem,
  // ...
  32: 8rem // new value
);
```

Then use the new spacing like `mt-32` in your HTML.



#### 📐 Breakpoints

- **sm**: ≤ 640px (mobile)
- **md**: ≤ 768px (tablet)
- **lg**: ≤ 1024px (desktop)



#### 📏 Spacing Scale

| Scale | rem  | px |
| ----- | ---- | -- |
| 0     | 0    | 0  |
| 1     | 0.25 | 4  |
| 2     | 0.5  | 8  |
| 3     | 0.75 | 12 |
| 4     | 1    | 16 |
| 5     | 1.25 | 20 |
| 6     | 1.5  | 24 |
| 8     | 2    | 32 |
| 10    | 2.5  | 40 |
| 12    | 3    | 48 |
| 16    | 4    | 64 |
| 20    | 5    | 80 |
| 24    | 6    | 96 |
