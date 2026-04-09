# CFRA2

> Utility-first CSS framework with brand tokens — Tailwind-compatible syntax, zero dependencies.

A single `<link>` or `npm install` gives you the full CFRA2 design system: navy/gold palette, 38 utility sections, 12 components, and Tailwind-identical class names so muscle memory just works.

> **Attribution:** CFRA2 is inspired by and built upon the utility-first methodology and class naming conventions of [Tailwind CSS](https://tailwindcss.com/) (MIT License, © Tailwind Labs Inc.). CFRA2 is an independent, pure-CSS implementation — it does not include or redistribute any Tailwind source code. It adds CFRA2-specific brand tokens, components, and design decisions on top of the familiar Tailwind class naming pattern.

---

## Installation

### npm (GitHub Packages)

```bash
npm install CFRA-2/cfra2-css
```

Then in your HTML:

```html
<link rel="stylesheet" href="node_modules/@cfra-2/cfra2-css/index.css">
```

Or import in a bundler:

```js
import '@cfra-2/cfra2-css';
```

### Direct link

```html
<link rel="stylesheet" href="https://cfra-2.github.io/cfra2-css/index.css">
```

---

## Design Tokens

All tokens are CSS custom properties on `:root`. Override them in your own stylesheet to theme the framework.

| Token | Value | Use |
|---|---|---|
| `--navy` | `#1a2744` | Primary brand color |
| `--navy-light` | `#243460` | Hover / lighter navy |
| `--navy-dark` | `#111b30` | Deep navy / tooltips |
| `--gold` | `#c8a84b` | Accent color |
| `--gold-light` | `#e2c97e` | Hover / lighter gold |
| `--bg` | `#e8ebf2` | Page background |
| `--white` | `#ffffff` | Surface white |
| `--text` | `#1c1c2e` | Default body text |
| `--muted` | `#6b7280` | Secondary text |
| `--border` | `#d1d5db` | Default border |
| `--success` | `#10b981` | Green |
| `--warning` | `#f59e0b` | Amber |
| `--danger` | `#ef4444` | Red |
| `--info` | `#3b82f6` | Blue |
| `--radius` | `8px` | Default border radius |
| `--radius-sm` | `4px` | Small radius |
| `--radius-lg` | `12px` | Large radius |
| `--radius-xl` | `16px` | Extra large radius |
| `--radius-full` | `9999px` | Pill |
| `--shadow` | `0 4px 24px …` | Default shadow |
| `--shadow-sm/md/lg/xl` | — | Shadow scale |
| `--font-sans` | Segoe UI, system-ui… | Sans-serif stack |
| `--font-mono` | Cascadia Code, Fira… | Monospace stack |
| `--sidebar-w` | `276px` | App sidebar width |

---

## Utilities Reference

### 1. Display
```html
<div class="block">
<div class="inline-block">
<div class="inline">
<div class="flex">
<div class="inline-flex">
<div class="grid">
<div class="hidden">        <!-- display: none -->
<div class="contents">
```

### 2. Visibility
```html
<div class="visible">
<div class="invisible">    <!-- visibility: hidden, space preserved -->
```

### 3. Position
```html
<div class="static | relative | absolute | fixed | sticky">
<div class="inset-0">      <!-- top/right/bottom/left: 0 -->
<div class="top-0 right-0 bottom-0 left-0">
<div class="top-auto left-auto">
```

### 4. Z-Index
```html
<div class="z-0 | z-10 | z-20 | z-30 | z-40 | z-50 | z-auto | z-top">
<!-- z-top = 9999 -->
```

### 5. Overflow
```html
<div class="overflow-auto | overflow-hidden | overflow-visible | overflow-scroll">
<div class="overflow-x-auto | overflow-x-hidden">
<div class="overflow-y-auto | overflow-y-hidden | overflow-y-scroll">
```

### 6. Flex
```html
<div class="flex flex-col gap-4 items-center justify-between">

<!-- Direction -->
flex-row | flex-row-reverse | flex-col | flex-col-reverse

<!-- Wrap -->
flex-wrap | flex-nowrap

<!-- Flex sizing -->
flex-1 | flex-auto | flex-initial | flex-none
shrink | shrink-0 | grow | grow-0

<!-- Align items -->
items-start | items-end | items-center | items-baseline | items-stretch

<!-- Justify content -->
justify-start | justify-end | justify-center | justify-between | justify-around | justify-evenly

<!-- Align self -->
self-auto | self-start | self-end | self-center | self-stretch
```

### 7. Grid
```html
<div class="grid grid-cols-3 gap-4">
  <div class="col-span-2">…</div>
  <div class="col-span-1">…</div>
</div>

<!-- Columns -->
grid-cols-1/2/3/4/5/6/12

<!-- Column span -->
col-span-1/2/3/4/6/full

<!-- Auto tracks -->
auto-cols-fr | auto-rows-fr
```

### 8. Gap
```html
gap-0/1/2/3/4/5/6/7/8/10/12/16
gap-x-0/1/2/3/4/6/8    <!-- column-gap -->
gap-y-0/1/2/3/4/6/8    <!-- row-gap -->
<!-- Scale: 1=4px  2=8px  3=12px  4=16px … 16=64px -->
```

### 9. Margin
```html
m-0/1/2/3/4/5/6/8/auto
mx-* | my-*           <!-- horizontal / vertical -->
mt-* | mr-* | mb-* | ml-*
<!-- Scale: 1=4px  2=8px  3=12px … 12=48px    auto=auto -->
```

### 10. Padding
```html
p-0/1/2/3/4/5/6/8/10/12
px-* | py-*
pt-* | pr-* | pb-* | pl-*
```

### 11. Width
```html
w-0 | w-4 | w-8 | w-16 | w-32 | w-64 | w-96
w-auto | w-full | w-screen | w-min | w-max | w-fit
w-1/2 | w-1/3 | w-2/3 | w-1/4 | w-3/4
min-w-0 | min-w-full | min-w-min | min-w-max
max-w-xs/sm/md/lg/xl/2xl/3xl/4xl/5xl/6xl/7xl/full/screen/none
```

### 12. Height
```html
h-0 | h-4 | h-8 | h-16 | h-32 | h-64 | h-96
h-auto | h-full | h-screen | h-svh | h-min | h-max | h-fit
min-h-0 | min-h-full | min-h-screen
max-h-32/48/64/96/full/screen
```

### 13. Font Size
```html
text-xs    → 12px
text-sm    → 13.5px
text-base  → 16px
text-lg    → 18px
text-xl    → 20px
text-2xl   → 24px
text-3xl   → 30px
text-4xl   → 36px
text-5xl   → 48px
text-6xl   → 60px
text-7xl   → 72px
text-8xl   → 96px
text-9xl   → 128px
```

### 14. Headings
```html
<h1 class="heading-1">Display heading</h1>
<h2 class="heading-2">Page title</h2>
<h3 class="heading-3">Section</h3>
<h4 class="heading-4">Subsection</h4>
<h5 class="heading-5">Label</h5>
<h6 class="heading-6">Small label</h6>

<!-- Color modifiers -->
<h2 class="heading-2 heading-gold">Gold heading</h2>
<h2 class="heading-2 heading-white">White heading</h2>
<h2 class="heading-2 heading-muted">Muted heading</h2>
```

### 15. Font Weight
```html
font-thin | font-extralight | font-light | font-normal
font-medium | font-semibold | font-bold | font-extrabold | font-black
```

### 16. Line Height
```html
leading-none | leading-tight | leading-snug | leading-normal | leading-relaxed | leading-loose
```

### 17. Letter Spacing
```html
tracking-tighter | tracking-tight | tracking-normal | tracking-wide | tracking-wider | tracking-widest
```

### 18. Text Align
```html
text-left | text-center | text-right | text-justify | text-start | text-end
```

### 19. Text Transform
```html
uppercase | lowercase | capitalize | normal-case
```

### 20. Text Decoration
```html
underline | line-through | no-underline
```

### 21. Text Overflow & Whitespace
```html
truncate            <!-- overflow:hidden + ellipsis + nowrap -->
whitespace-normal | whitespace-nowrap | whitespace-pre | whitespace-pre-wrap
break-words | break-all | break-keep
```

### 22. Font Family
```html
font-sans   → Segoe UI, system-ui…
font-mono   → Cascadia Code, Fira Code…
font-serif  → Georgia, Cambria…
```

### 23. Text Color
```html
text-navy | text-navy-light | text-navy-dark
text-gold | text-gold-light
text-white | text-black | text-muted | text-text
text-success | text-warning | text-danger | text-info
text-inherit | text-current | text-transparent
```

### 24. Background Color
```html
bg-navy | bg-navy-light | bg-navy-dark
bg-gold | bg-gold-light
bg-white | bg-black | bg-bg | bg-transparent
bg-success | bg-warning | bg-danger | bg-info
```

### 25. Border
```html
border          <!-- 1px solid --border -->
border-0        <!-- no border -->
border-2        <!-- 2px solid -->
border-t | border-r | border-b | border-l

<!-- Colors -->
border-navy | border-gold | border-white | border-transparent
border-success | border-warning | border-danger | border-info

<!-- Style -->
border-solid | border-dashed | border-dotted | border-none
```

### 26. Border Radius
```html
rounded-none | rounded-sm | rounded | rounded-lg | rounded-xl | rounded-full
rounded-t | rounded-b | rounded-l | rounded-r
```

### 27. Ring (focus outline)
```html
ring          <!-- gold ring -->
ring-navy | ring-gold | ring-danger | ring-white | ring-0
```

### 28. Shadow
```html
shadow-none | shadow-sm | shadow | shadow-md | shadow-lg | shadow-xl
```

### 29. Opacity
```html
opacity-0/5/10/20/25/30/40/50/60/70/75/80/90/95/100
```

### 30. Cursor
```html
cursor-auto | cursor-default | cursor-pointer | cursor-wait
cursor-text | cursor-move | cursor-not-allowed | cursor-grab | cursor-grabbing
```

### 31. User Select & Pointer Events
```html
select-none | select-text | select-all | select-auto
pointer-events-none | pointer-events-auto
```

### 32. Transition
```html
transition          <!-- sensible defaults -->
transition-none | transition-all | transition-colors | transition-opacity | transition-shadow | transition-transform
duration-75/100/150/200/300/500/700
ease-linear | ease-in | ease-out | ease-in-out
```

### 33. Transform
```html
scale-0/50/75/90/95/100/105/110/125/150
rotate-0/45/90/180  |  -rotate-45/-rotate-90
translate-x-0 | translate-y-0 | -translate-y-1 | -translate-y-2 | translate-y-full
```

### 34. Filter
```html
blur-none | blur-sm | blur | blur-md | blur-lg | blur-xl
backdrop-blur-sm | backdrop-blur | backdrop-blur-md | backdrop-blur-lg
```

### 35. Object Fit
```html
object-contain | object-cover | object-fill | object-none | object-scale
object-center | object-top | object-bottom
```

### 36. Aspect Ratio
```html
aspect-auto | aspect-square | aspect-video | aspect-4-3
```

### 37. List Style
```html
list-none | list-disc | list-decimal | list-inside | list-outside
```

### 38. Scroll
```html
scroll-smooth | scroll-auto
scroll-thin   <!-- 4px scrollbar -->
scroll-base   <!-- 6px scrollbar -->
overscroll-auto | overscroll-contain | overscroll-none
```

---

## Components Reference

### Card
```html
<!-- Light card -->
<div class="card p-4">
  Content
</div>

<!-- Dark (navy) card -->
<div class="card-dark">
  <div class="card-section">Section A</div>
  <div class="card-section">Section B</div>
</div>
```

### Panel Header
```html
<div class="panel-header">
  <div class="panel-title">My Panel</div>
  <div class="panel-subtitle">Subtitle</div>
</div>
```

### Section Label
```html
<div class="section-label">Configuration</div>
```

### Field + Input
```html
<div class="field">
  <label class="field-label">Name</label>
  <input class="field-input" type="text" placeholder="Enter name">
</div>

<!-- Dark variant (on navy backgrounds) -->
<div class="field">
  <label class="field-label">Name</label>
  <input class="field-input field-input--dark" type="text">
</div>
```

### Buttons
```html
<button class="btn btn-navy">Primary</button>
<button class="btn btn-gold">Accent</button>
<button class="btn btn-outline">Outline</button>
<button class="btn btn-ghost">Ghost</button>
<button class="btn btn-danger">Delete</button>

<!-- Sizes -->
<button class="btn btn-navy btn-sm">Small</button>
<button class="btn btn-navy btn-lg">Large</button>

<!-- Icon button (toolbar) -->
<button class="btn-icon active">⚙</button>
```

### Badge
```html
<span class="badge badge-success">Active</span>
<span class="badge badge-warning">Pending</span>
<span class="badge badge-danger">Error</span>
<span class="badge badge-info">Info</span>
<span class="badge badge-navy">Navy</span>
<span class="badge badge-gold">Gold</span>
```

### Toast
```html
<div class="toast">Default message</div>
<div class="toast toast-ok">Saved successfully</div>
<div class="toast toast-err">Something went wrong</div>
<div class="toast toast-warn">Warning message</div>
```

### Divider
```html
<hr class="divider">           <!-- light background -->
<hr class="divider-dark">     <!-- navy background -->
<span class="divider-v"></span> <!-- vertical inline divider -->
```

### Toggle Switch
```html
<label class="toggle">
  <input type="checkbox">
  <span class="toggle-track">
    <span class="toggle-thumb"></span>
  </span>
  Enable feature
</label>
```

### Overlay / Modal Backdrop
```html
<div class="overlay">
  <div class="card-dark p-6">
    Modal content here
  </div>
</div>
```

### Tooltip
```html
<span data-tip="This is the tooltip text">Hover me</span>
```

### Animations
```html
<div class="animate-fade-in">Fades in from bottom</div>
<div class="animate-scale-in">Scales in from center</div>
<div class="animate-slide-down">Slides in from top</div>
<div class="animate-spin">Spinning loader</div>
<div class="animate-pulse">Pulsing element</div>
<div class="animate-bounce">Bouncing element</div>
<div class="animate-none">No animation</div>
```

---

## Common Patterns

### App shell (sidebar + main)
```html
<div class="flex h-screen overflow-hidden">
  <aside class="flex-col bg-navy" style="width: var(--sidebar-w)">
    <!-- sidebar content -->
  </aside>
  <main class="flex-1 overflow-y-auto bg-bg p-6">
    <!-- main content -->
  </main>
</div>
```

### Responsive card grid
```html
<div class="grid grid-cols-3 gap-6">
  <div class="card p-4">Card 1</div>
  <div class="card p-4">Card 2</div>
  <div class="card p-4">Card 3</div>
</div>
```

### Form with dark inputs
```html
<div class="card-dark p-6">
  <h3 class="heading-3 heading-white mb-4">Settings</h3>
  <div class="field">
    <label class="field-label">Username</label>
    <input class="field-input field-input--dark" type="text">
  </div>
  <div class="flex gap-3 mt-4">
    <button class="btn btn-gold">Save</button>
    <button class="btn btn-ghost">Cancel</button>
  </div>
</div>
```

### Notification toast (JS-driven)
```html
<div id="toast" class="toast toast-ok hidden">
  Operation completed
</div>
<script>
  // show
  document.getElementById('toast').classList.remove('hidden');
  document.getElementById('toast').classList.add('animate-fade-in');
  // hide after 3s
  setTimeout(() => document.getElementById('toast').classList.add('hidden'), 3000);
</script>
```

---

## Backward Compatibility

CFRA2 v2 keeps v1 class names as aliases so existing code keeps working:

| v1 (legacy) | v2 (current) |
|---|---|
| `uk-btn` | `btn` |
| `uk-btn-navy` | `btn-navy` |
| `uk-btn-out` | `btn-outline` |
| `uk-btn-ghost` | `btn-ghost` |
| `uk-btn-danger` | `btn-danger` |
| `uk-btn-icon` | `btn-icon` |
| `uk-badge` | `badge` |
| `uk-badge-success` etc. | `badge-success` etc. |
| `uk-toast` | `toast` |
| `uk-toast-ok` | `toast-ok` |
| `uk-toast-err` | `toast-err` |
| `uk-toggle` | `toggle` |
| `uk-toggle-track` | `toggle-track` |
| `uk-toggle-thumb` | `toggle-thumb` |
| `uk-overlay` | `overlay` |
| `animate-fadeInUp` | `animate-fade-in` |
| `animate-scaleIn` | `animate-scale-in` |

---

## License

MIT © CFRA-2
