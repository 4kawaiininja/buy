# 🎨 KawaiiNinja Dark Theme - Detailed Documentation

This document provides a comprehensive guide to the KawaiiNinja Dark Theme, outlining its design philosophy, color palette, typography, and detailed usage instructions for each component. This theme is built with Tailwind CSS for rapid development and consistent styling.

---

## 📚 Table of Contents

1. [🎯 Theme Philosophy](#-theme-philosophy)
   - [Design Principles](#design-principles)
   - [Visual Characteristics](#visual-characteristics)
2. [🎨 Color Palette](#-color-palette)
3. [🔠 Typography](#-typography)
4. [🧩 Component Usage](#-component-usage)
   - [Main Container Structure](#1-main-container-structure)
   - [Section Headers](#2-section-headers)
   - [Content Cards](#3-content-cards)
   - [Form Elements](#4-form-elements)
   - [Stat Cards](#5-stat-cards)
   - [Status Badges](#6-status-badges)
   - [Info Notes](#7-info-notes)
   - [Custom Checkboxes](#8-custom-checkboxes-random-accent-glow)
   - [Toggle Switches](#9-toggle-switches)
   - [Clean Selection Cards](#10-clean-selection-cards)
   - [Quick Analytics Cards](#11-quick-analytics-cards-with-random-hover-colors)
   - [FieldGridPreview](#12-fieldgridpreview)
5. [🛠️ General Usage Rules](#%EF%B8%8F-general-usage-rules)

---

## 🎯 Theme Philosophy

The KawaiiNinja Dark Theme is designed with a focus on a modern, clean, minimal, and professional aesthetic, infused with a tech-inspired cyber/tech-punk vibe and subtle neon accents.

### Design Principles

- **Minimal & Clean**: Reduced visual clutter with purposeful spacing and clear hierarchy.
- **Dark & Professional**: Optimized for low-light environments with high contrast for readability.
- **Tech-Inspired**: Incorporates elements that evoke a cyber/tech-punk feel, often with neon highlights.
- **Organized**: Ensures clear visual hierarchy and consistent patterns across all components.
- **Extensible**: Designed for easy addition of new components while maintaining overall consistency.

### Visual Characteristics

- Predominantly black/dark backgrounds with subtle transparency.
- Light white borders for defining elements and sections.
- Consistent spacing, padding, and typography.
- Smooth transitions and hover states for interactive elements.
- Professional and sleek styling for buttons and form elements.

---

## 🎨 Color Palette

The theme utilizes a carefully selected color palette to achieve its distinct dark and tech-inspired look.

| Tailwind Class           | Color Value                 | Description                                        |
| ------------------------ | --------------------------- | -------------------------------------------------- |
| `bg-body`                | `#0e0e0e`                   | Main background for the entire application.        |
| `text-primary`           | `#ffffff`                   | Primary text color, high contrast.                 |
| `text-secondary`         | `rgba(255, 255, 255, 0.7)`  | Secondary text for descriptions and less emphasis. |
| `text-secondary/60`      | `rgba(255, 255, 255, 0.6)`  | Even lighter secondary text.                       |
| `bg-accent`              | `#06b6d4`                   | Primary accent color (cyan/teal).                  |
| `bg-accent/10`           | `rgba(6, 182, 212, 0.1)`    | Light accent background.                           |
| `bg-white/[0.02]`        | `rgba(255, 255, 255, 0.02)` | Subtle transparent white background for cards.     |
| `border-white/5`         | `rgba(255, 255, 255, 0.05)` | Thin, subtle white border.                         |
| `bg-black/5`             | `rgba(0, 0, 0, 0.05)`       | Very subtle black background for inputs.           |
| `border-white/10`        | `rgba(255, 255, 255, 0.1)`  | Slightly more prominent white border.              |
| `hover:bg-white/[0.04]`  | `rgba(255, 255, 255, 0.04)` | Hover state for interactive cards.                 |
| `focus:ring-accent`      | `#06b6d4`                   | Focus ring color for inputs.                       |
| `hover:border-accent/50` | `rgba(6, 182, 212, 0.5)`    | Hover border for inputs.                           |
| `bg-red-400/50`          | `rgba(248, 113, 113, 0.5)`  | Error background.                                  |
| `text-red-400`           | `#f87171`                   | Error text color.                                  |
| `bg-green-400/20`        | `rgba(74, 222, 128, 0.2)`   | Success badge background.                          |
| `text-green-400`         | `#4ade80`                   | Success badge text.                                |
| `bg-yellow-400/20`       | `rgba(250, 204, 21, 0.2)`   | Warning badge background.                          |
| `text-yellow-400`        | `#facc15`                   | Warning badge text.                                |
| `bg-blue-400/20`         | `rgba(96, 165, 250, 0.2)`   | Info badge background.                             |
| `text-blue-400`          | `#60a5fa`                   | Info badge text.                                   |
| `bg-purple-400/20`       | `rgba(192, 132, 252, 0.2)`  | Example analytics card border.                     |
| `text-purple-400`        | `#c084fc`                   | Example analytics card text.                       |

---

## 🔠 Typography

The theme uses the Inter font for all text, ensuring readability and a modern feel.

```css
body {
  font-family: "Inter", sans-serif;
}
```

Font weights and sizes are controlled via Tailwind CSS utility classes (e.g., `font-bold`, `text-lg`, `text-xs`).

---

## 🧩 Component Usage

All components are designed to be responsive and integrate seamlessly with the dark theme. They leverage Tailwind CSS classes extensively.

### 1. Main Container Structure

This is the primary wrapper for full-page content.

**Usage:**

Apply `card bg-transparent border border-white/5` to your main content div. Use responsive column classes (`col-span-1 sm:col-span-2 lg:col-span-4`) as needed for layout.

```html
<div
  class="card bg-transparent border border-white/5 col-span-1 sm:col-span-2 lg:col-span-4 flex flex-col flex-grow max-h-max overflow-hidden fade-in"
>
  <div class="relative flex-grow overflow-auto custom-scrollbar">
    <!-- Your content here -->
  </div>
</div>
```

### 2. Section Headers

Provides clear headings and descriptions for different sections of your application.

**Usage:**

- **Page Header with Icon:** Use `flex items-center` for the container, `bg-accent/10 rounded-md` for the icon wrapper, and `text-lg font-semibold text-primary` for the title.
- **Section Divider with Colored Indicator:** Use `w-1 h-4 bg-blue-400 rounded` for the vertical indicator and `text-sm font-medium text-primary` for the heading.

```html
<!-- Page header with icon and description -->
<div class="flex items-center mb-6">
  <div
    class="flex items-center justify-center w-8 h-8 bg-accent/10 rounded-md mr-3"
  >
    <!-- SVG Icon -->
  </div>
  <div>
    <h1 class="text-lg font-semibold text-primary">Dashboard Overview</h1>
    <p class="text-xs text-secondary/60">
      A quick glance at your key metrics and recent activities.
    </p>
  </div>
</div>

<!-- Section divider with colored indicator -->
<div class="settings-section">
  <div class="flex items-center mb-4">
    <div class="w-1 h-4 bg-blue-400 rounded mr-3"></div>
    <h2 class="text-sm font-medium text-primary">General Settings</h2>
  </div>
  <p class="text-secondary/70">
    Manage your account preferences and basic information here.
  </p>
</div>
```

### 3. Content Cards

Versatile cards for grouping content.

**Usage:**

Apply `bg-white/[0.02] border border-white/5 rounded-lg p-4` for basic styling. Add `hover:bg-white/[0.04] transition-colors cursor-pointer` for interactive cards.

```html
<!-- Standard content card -->
<div class="bg-white/[0.02] border border-white/5 rounded-lg p-4">
  <h3 class="text-sm font-medium text-secondary mb-3">Basic Information</h3>
  <p class="text-secondary/70">This is a standard content card.</p>
</div>

<!-- Interactive content card with hover -->
<div
  class="bg-white/[0.02] border border-white/5 rounded-lg p-4 hover:bg-white/[0.04] transition-colors cursor-pointer"
>
  <h3 class="text-sm font-medium text-secondary mb-3">Interactive Card</h3>
  <p class="text-secondary/70">This card has a subtle hover effect.</p>
</div>
```

### 4. Form Elements

Styled inputs, selects, and buttons.

**Usage:**

- **Input Fields:** Use `w-full px-3 py-2 text-sm bg-black/5 border border-white/5 rounded text-primary/80 focus:outline-none focus:ring-2 focus:ring-accent hover:border-accent/50 transition-colors`. For error states, replace `border-white/5` with `border-red-400/50` and `text-primary/80` with `text-red-400`.
- **Select Dropdowns:** Use `dark-select px-3 py-2 bg-black/5 border border-white/5 rounded text-sm text-primary focus:outline-none hover:border-accent/50 transition-colors w-full`. The `dark-select` class in `<style>` ensures options match the dark background.
- **Buttons:** Use `px-4 py-2 bg-accent text-white rounded text-sm font-medium hover:bg-accent/80 transition-colors`.

```html
<!-- Text Input -->
<input
  type="text"
  class="w-full px-3 py-2 text-sm bg-black/5 border border-white/5 rounded text-primary/80 focus:outline-none focus:ring-2 focus:ring-accent hover:border-accent/50 transition-colors"
/>

<!-- Error Input -->
<input
  type="email"
  class="w-full px-3 py-2 text-sm bg-black/5 border border-red-400/50 rounded text-red-400 focus:outline-none focus:ring-2 focus:ring-red-400"
/>
<p class="text-xs text-red-400/80">Error message.</p>

<!-- Select Dropdown -->
<select
  class="dark-select px-3 py-2 bg-black/5 border border-white/5 rounded text-sm text-primary focus:outline-none hover:border-accent/50 transition-colors w-full"
>
  <option>Option 1</option>
</select>

<!-- Button -->
<button
  class="px-4 py-2 bg-accent text-white rounded text-sm font-medium hover:bg-accent/80 transition-colors"
>
  Submit Form
</button>
```

### 5. Stat Cards

Displays key metrics with a clear hierarchy. Cards can optionally include a trend indicator to reflect performance changes.

**Usage:**

Apply `bg-white/[0.02] border border-white/5 rounded-lg p-4` to the card container.  
Use a label bar with `flex items-center mb-2` for the metric title.  
To display trends, add an inline arrow icon and percentage below the value using `flex items-center justify-center mt-1 space-x-1`.

Basic usage:

```html
<div class="bg-white/[0.02] border border-white/5 rounded-lg p-4">
  <div class="flex items-center mb-2">
    <div class="w-1 h-4 bg-blue-400 rounded mr-3"></div>
    <h2 class="text-sm font-medium text-primary">Total Users</h2>
  </div>
  <span class="text-2xl font-bold text-accent block text-center">1,234</span>
</div>
```

Trend Indicator:

```html
<div class="bg-white/[0.02] border border-white/5 rounded-lg p-4">
  <div class="flex items-center mb-2">
    <div class="w-1 h-4 bg-blue-400 rounded mr-3"></div>
    <h2 class="text-sm font-medium text-primary">Total Users</h2>
  </div>
  <span class="text-2xl font-bold text-accent block text-center">1,234</span>
  <div class="flex items-center justify-center mt-1 space-x-1">
    <!-- Down arrow SVG -->
    <svg
      class="w-3 h-3 text-red-400"
      fill="none"
      viewBox="0 0 24 24"
      stroke="currentColor"
      stroke-width="3"
    >
      <path stroke-linecap="round" stroke-linejoin="round" d="M19 9l-7 7-7-7" />
    </svg>

    <!-- Up arrow SVG -->
    <svg
      class="w-3 h-3 text-green-400"
      fill="none"
      viewBox="0 0 24 24"
      stroke="currentColor"
      stroke-width="3"
    >
      <path stroke-linecap="round" stroke-linejoin="round" d="M5 15l7-7 7 7" />
    </svg>

    <span class="text-xs text-red-400 font-medium">−2.1%</span>
    <span class="text-xs text-white/50">since last week</span>
  </div>
</div>
```

### 6. Status Badges

Small, colored indicators for various statuses.

**Usage:**

Apply `px-2 py-1 rounded text-xs font-medium` along with specific `bg-*`, `text-*`, and `border-*` classes for different statuses (e.g., `bg-green-400/20 text-green-400 border border-green-400/30` for success).

```html
<span
  class="px-2 py-1 rounded text-xs font-medium bg-green-400/20 text-green-400 border border-green-400/30"
  >Completed</span
>
<span
  class="px-2 py-1 rounded text-xs font-medium bg-yellow-400/20 text-yellow-400 border border-yellow-400/30"
  >In Progress</span
>
<span
  class="px-2 py-1 rounded text-xs font-medium bg-red-400/20 text-red-400 border border-red-400/30"
  >Failed</span
>
<span
  class="px-2 py-1 rounded text-xs font-medium bg-blue-400/20 text-blue-400 border border-blue-400/30"
  >Info</span
>
```

### 7. Info Notes

Provides helpful contextual information or instructions.

**Usage:**

Wrap your text and SVG inside a div with `flex items-center text-xs text-secondary/60`. Place this within a div that has `mt-4 pt-3 border-t border-white/5` for a subtle separator.

```html
<div class="mt-4 pt-3 border-t border-white/5">
  <div class="flex items-center text-xs text-secondary/60">
    <svg
      class="w-3 h-3 mr-1.5"
      fill="none"
      stroke="currentColor"
      viewBox="0 0 24 24"
    >
      <path
        stroke-linecap="round"
        stroke-linejoin="round"
        stroke-width="2"
        d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
      ></path>
    </svg>
    Your informational message text here.
  </div>
</div>
```

### 8. Custom Checkboxes (Random Accent Glow)

Interactive checkboxes with a unique visual style and a dynamic accent glow.

**Usage:**

- The actual `<input type="checkbox">` should have `class="sr-only peer"`.
- The visual representation is a div with `id="colorBox-{id}"` (e.g., `colorBox-email-notif`) and classes like `relative w-4 h-4 rounded border border-white/10 bg-black/5 flex items-center justify-center`.
- The SVG checkmark inside this div has `opacity-0 peer-checked:opacity-100`.
- The JavaScript handles the random color glow on `peer-checked`.
- For checkboxes within `FieldGridPreview` or `Attributes Dummy Example`, they are wrapped in a div with `flex items-center justify-between border border-white/10 rounded-md p-2 w-full` to ensure the full-width bordered container and spaced layout.

```html
<label
  class="flex items-center justify-between w-full px-2 py-2 border border-white/10 rounded-md cursor-pointer group"
>
  <div class="flex items-center justify-between w-full">
    <input type="checkbox" id="checkbox-email-notif" class="sr-only peer" />
    <div
      id="colorBox-email-notif"
      class="relative w-4 h-4 rounded border border-white/10 bg-black/5 flex items-center justify-center peer-focus:outline-none peer-focus:ring-2 peer-focus:ring-accent peer-focus:ring-offset-2 peer-focus:ring-offset-black/10 peer-checked:w-10 peer-checked:rounded-xl peer-checked:px-2 transition-all duration-300 ease-in-out"
    >
      <svg
        class="h-3 w-3 text-white opacity-0 peer-checked:opacity-100 transition-opacity duration-200"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
        stroke-width="3"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          d="M5 13l4 4L19 7"
        />
      </svg>
    </div>
    <span class="text-sm text-primary ml-auto"
      >Email notifications for payouts</span
    >
  </div>
</label>
```

JavaScript for Custom Checkboxes:

Ensure the `checkboxColorCombos` array in the `<script>` tag includes the `boxId` and `checkId` for every custom checkbox you use.

```javascript
const checkboxColorCombos = [
  { boxId: "colorBox-email-notif", checkId: "checkbox-email-notif" },
  // ... add other custom checkboxes here
];

checkboxColorCombos.forEach(({ boxId, checkId }) => {
  const checkbox = document.getElementById(checkId);
  const box = document.getElementById(boxId);
  // ... (rest of the JS logic)
});
```

### 9. Toggle Switches

Compact and interactive toggle switches.

**Usage:**

- The actual `<input type="checkbox">` should have `class="sr-only peer"`.
- The visual switch track is a div with `w-7 h-4 bg-gray-600/50 peer-focus:outline-none rounded-full peer-checked:bg-green-500 transition-colors relative`.
- The movable thumb is a nested div with `absolute w-3 h-3 bg-white rounded-full shadow-md transform transition-transform duration-300 ease-in-out left-[2px] top-1/2 -translate-y-1/2 peer-checked:translate-x-[16px]`.

```html
<label class="relative inline-flex items-center cursor-pointer">
  <input type="checkbox" id="compactToggle" class="sr-only peer" />
  <div
    class="w-7 h-4 bg-gray-600/50 peer-focus:outline-none rounded-full peer-checked:bg-green-500 transition-colors relative"
  >
    <div
      class="absolute w-3 h-3 bg-white rounded-full shadow-md transform transition-transform duration-300 ease-in-out left-[2px] top-1/2 -translate-y-1/2 peer-checked:translate-x-[16px]"
    ></div>
  </div>
</label>
<span class="ml-2 text-sm text-primary">Compact Toggle</span>
```

### 10. Clean Selection Cards

Interactive cards for single or multiple selections, with a clear selected state.

**Usage:**

- Apply `selection-card` to the `<label>` element.
- The actual `<input type="checkbox">` should have `class="selection-checkbox"`.
- The `card-content` div handles the layout of the title, description, and icon.
- The `selection-card.selected` CSS class is toggled by JavaScript to indicate selection.

```html
<label class="selection-card" data-option="option1">
  <input type="checkbox" class="selection-checkbox" />
  <div class="card-content">
    <div class="option-info">
      <h4>Option Title One</h4>
      <p>Option description or details for option one.</p>
    </div>
    <i class="option-icon">🎯</i>
  </div>
</label>
```

JavaScript for Clean Selection Cards:

This script handles the toggling of the `selected` class based on checkbox state.

```javascript
document.querySelectorAll(".selection-card").forEach((card) => {
  const checkbox = card.querySelector(".selection-checkbox");
  if (checkbox.checked) card.classList.add("selected");

  card.addEventListener("click", function (e) {
    // ... (rest of the JS logic)
  });
});
```

### 11. Quick Analytics Cards (with Random Hover Colors)

Small cards for quick data display, featuring a dynamic hover effect.

**Usage:**

Apply `quick-analytics-card flex flex-col bg-black/5 border rounded-lg p-3 transition-colors duration-300 cursor-pointer` to the card container, along with a specific `border-*` class (e.g., `border-purple-400/20`).

```html
<div
  class="quick-analytics-card flex flex-col bg-black/5 border border-purple-400/20 rounded-lg p-3 transition-colors duration-300 cursor-pointer"
>
  <span class="text-xs text-secondary/70 mb-1 uppercase tracking-wide"
    >Top Category</span
  >
  <span class="text-base font-bold text-accent">Fashion</span>
</div>
```

JavaScript for Quick Analytics Cards:

This script applies a random background color from a predefined list on hover.

```javascript
const quickAnalyticsCards = document.querySelectorAll(".quick-analytics-card");
const hoverColors = [
  "rgba(139, 92, 246, 0.18)", // purple
  // ... add other hover colors
];
quickAnalyticsCards.forEach((card) => {
  card.addEventListener("mouseenter", () => {
    // ... (rest of the JS logic)
  });
  card.addEventListener("mouseleave", () => {
    // ... (rest of the JS logic)
  });
});
```

### 12. FieldGridPreview

A versatile grid layout for displaying groups of form elements or attributes.

**Usage:**

Apply `grid grid-cols-1 md:grid-cols-4 gap-2 bg-white/[0.02] border border-white/5 rounded-lg px-3 py-2` to the main container. Each child element (input, select, checkbox container, button) will automatically align within the grid. For disabled states, add `opacity-60 pointer-events-none`.

```html
<div
  class="grid grid-cols-1 md:grid-cols-4 gap-2 bg-white/[0.02] border border-white/5 rounded-lg px-3 py-2"
>
  <input
    type="text"
    placeholder="Text Field"
    class="px-2 py-1 rounded-md bg-black/10 border border-white/10 text-primary text-xs w-full"
  />
  <select
    class="dark-select px-2 py-1 rounded-md bg-black/10 border border-white/10 text-primary text-xs w-full"
  >
    <option>Option 1</option>
  </select>
  <!-- Custom Checkbox as described in section 8 -->
  <div
    class="flex items-center justify-between border border-white/10 rounded-md p-2 w-full"
  >
    <label
      class="flex items-center justify-between w-full cursor-pointer group text-xs text-secondary"
    >
      <div class="flex items-center">
        <input type="checkbox" id="fieldGridCheckbox" class="sr-only peer" />
        <div
          id="colorBox-fieldGridCheckbox"
          class="relative w-4 h-4 rounded border border-white/10 bg-black/5 flex items-center justify-center peer-focus:outline-none peer-focus:ring-2 peer-focus:ring-accent peer-focus:ring-offset-2 peer-focus:ring-offset-black/10 peer-checked:w-10 peer-checked:rounded-xl peer-checked:px-2 transition-all duration-300 ease-in-out"
        >
          <svg
            class="h-3 w-3 text-white opacity-0 peer-checked:opacity-100 transition-opacity duration-200"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="3"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M5 13l4 4L19 7"
            />
          </svg>
        </div>
      </div>
      <span>Checkbox</span>
    </label>
  </div>
  <button
    type="button"
    class="text-accent text-xs rounded-md px-2 py-1 bg-black/5 border border-white/10 w-full"
  >
    Action
  </button>
</div>
```

## 🛠️ General Usage Rules

- **Tailwind CSS First**: Prioritize using Tailwind's utility-first classes for styling. Custom CSS should be minimal and used only when Tailwind doesn't offer a direct solution (e.g., for scrollbar styling or complex pseudo-elements).
- **CDN Inclusion**: Ensure the Tailwind CSS CDN is included in your `<head>` tag:
  ```html
  <script src="https://cdn.tailwindcss.com"></script>
  ```
- **Font Inclusion**: The Inter font is loaded via Google Fonts:
  ```html
  <link
    href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap"
    rel="stylesheet"
  />
  ```
- **Responsiveness**: All components are designed with responsiveness in mind, utilizing Tailwind's responsive prefixes (`sm:`, `md:`, `lg:`) for adaptive layouts. Always test on various screen sizes.
- **JavaScript for Interactivity**: Components with dynamic behavior (e.g., custom checkboxes, quick analytics cards) rely on basic JavaScript. Ensure the provided `<script>` block is included at the end of your `<body>` tag.
- **Accessibility**: While not explicitly detailed for every component, strive for accessibility. Ensure proper ARIA attributes, keyboard navigation, and sufficient color contrast where needed.
- **Custom Scrollbar**: The custom scrollbar styling is applied globally to elements with the `custom-scrollbar` class. Add this class to any div that has `overflow-auto` or `overflow-y-auto` to apply the themed scrollbar.

This documentation should provide a clear understanding of the KawaiiNinja Dark Theme and how to effectively use its components in your projects.
