# 🎨 Official Theme Collection

## Theme Names & Variants

### **Primary Theme Options:**

- **🥷 Kuro - Dark Theme** (Japanese-inspired, matches anime aesthetic)
- **⚫ Ninja - Dark Theme** (Brand-aligned, stealth aesthetic)
- **🖤 Carbon - Theme** (Professional, material-inspired)

_All three variants use the same underlying design system with identical implementation._

---

## Overview

This document outlines the complete dark theme system used across the KawaiiNinja admin/partner dashboard. The theme collection is designed to be modern, clean, minimal, and professional with a tech-inspired aesthetic.

**Theme Identity:** Choose from Kuro, Ninja, or Carbon based on your preference - all share the same robust design foundation.

---

## 🎯 Theme Philosophy

### Design Principles

- **Minimal & Clean**: Reduced visual clutter with purposeful spacing
- **Dark & Professional**: Low-light friendly with high contrast
- **Tech-Inspired**: Cyber/tech-punk aesthetic with neon accents
- **Organized**: Clear visual hierarchy and consistent patterns
- **Extensible**: Easy to add new components while maintaining consistency

### Visual Characteristics

- Black/dark backgrounds with subtle transparency
- Light white borders for definition
- Consistent spacing and typography
- Smooth transitions and hover states
- Professional button and form styling

---

## 🎨 Color Palette

### Primary Colors

```css
/* Main Background Colors */
bg-transparent                    /* Transparent background for main containers */
bg-white/[0.02]                  /* Very subtle white overlay (2% opacity) */
bg-black/5                       /* Subtle black overlay (5% opacity) */
bg-black/10                      /* Slightly stronger black overlay (10% opacity) */
bg-black/20                      /* Progress bar backgrounds */

/* Border Colors */
border-white/5                   /* Primary border color (5% white opacity) */
border-white/10                  /* Stronger borders when needed */
```

### Text Colors

```css
/* Text Hierarchy */
text-primary                     /* Main headings and important text */
text-secondary                   /* Subheadings and regular content */
text-secondary/60               /* Muted descriptions and labels */
text-secondary/70               /* Body text with medium emphasis */
text-secondary/80               /* Labels and form text */
text-secondary/50               /* Very muted text */

/* Special Text */
text-accent                     /* Accent color for highlights and CTAs */
```

### Semantic Colors

```css
/* Status & Feedback Colors */
text-green-400                  /* Success states, completed items */
bg-green-400/20                 /* Success background with transparency */
border-green-400/30             /* Success borders */

text-yellow-400                 /* Warning states, in-progress items */
bg-yellow-400/20                /* Warning background */
border-yellow-400/30            /* Warning borders */

text-red-400                    /* Error states, failed items */
bg-red-400/20                   /* Error background */
border-red-400/30               /* Error borders */

text-blue-400                   /* Info states, general highlights */
text-cyan-400                   /* Alternative accent color */
text-purple-400                 /* Secondary accent for variety */
```

### Section Indicators

```css
/* Colored bars for section identification */
bg-blue-400                     /* General/Overview sections */
bg-cyan-400                     /* Primary content sections */
bg-yellow-400                   /* Active/Current sections */
bg-green-400                    /* Completed/History sections */
bg-purple-400                   /* Instructions/Help sections */
```

---

## ✒️ Typography

To maintain a consistent and tech-inspired aesthetic, the theme utilizes the following font stack:

```css
/* Primary Font */
font-family:
   'Inter', 'Segoe UI', Roboto, 'Helvetica Neue', Arial, 'Noto Sans', sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol',
   'Noto Color Emoji';

/* Monospace Font (for code snippets, etc.) */
font-family: 'Fira Code', 'JetBrains Mono', 'SFMono-Regular', Consolas, 'Liberation Mono', Menlo, Courier, monospace;
```

---

## 🧩 Component Patterns

### Main Container Structure

```html
<!-- Primary container for full pages -->
<div
   class="card bg-transparent border border-white/5 col-span-1 sm:col-span-2 lg:col-span-4 flex flex-col flex-grow max-h-max overflow-hidden fade-in"
>
   <div class="relative flex-grow overflow-auto custom-scrollbar">
      <div class="p-4 space-y-6">
         <!-- Content goes here -->
      </div>
   </div>
</div>
```

### Section Headers

```html
<!-- Page header with icon and description -->
<div class="flex items-center mb-6">
   <div class="flex items-center justify-center w-8 h-8 bg-accent/10 rounded-md mr-3">
      <!-- SVG icon here -->
   </div>
   <div>
      <h1 class="text-lg font-semibold text-primary">Page Title</h1>
      <p class="text-xs text-secondary/60">Page description</p>
   </div>
</div>

<!-- Section divider with colored indicator -->
<div class="settings-section">
   <div class="flex items-center mb-4">
      <div class="w-1 h-4 bg-blue-400 rounded mr-3"></div>
      <h2 class="text-sm font-medium text-primary">Section Title</h2>
   </div>
   <!-- Section content -->
</div>
```

### Content Cards

```html
<!-- Standard content card -->
<div class="bg-white/[0.02] border border-white/5 rounded-lg p-4">
   <h3 class="text-sm font-medium text-secondary mb-3">Card Title</h3>
   <!-- Card content -->
</div>

<!-- Interactive content card with hover -->
<div class="bg-white/[0.02] border border-white/5 rounded-lg p-4 hover:bg-white/[0.04] transition-colors">
   <!-- Content -->
</div>
```

### Form Elements

````html
<!-- Input fields -->
<input
   class="w-full px-3 py-2 text-sm bg-black/5 border border-white/5 rounded text-primary/80 focus:outline-none focus:ring-2 focus:ring-accent hover:border-accent/50 transition-colors"
/>

<!-- Error Input fields -->
<div class="space-y-1">
   <input
      class="w-full px-3 py-2 text-sm bg-black/5 border border-red-400/50 rounded text-red-400 focus:outline-none focus:ring-2 focus:ring-red-400"
      value="example@domain"
   />
   <p class="text-xs text-red-400/80">Please enter a valid email address.</p>
</div>

<!-- Dark Select dropdowns -->
<select
   class="dark-select px-3 py-2 bg-black/5 border border-white/5 rounded text-sm text-primary focus:outline-none hover:border-accent/50 transition-colors"
>
   <option>Option 1</option>
</select>

<!-- Dark Select -->
```css
<style>
   select.dark-select option {
      background-color: #0e0e0e;
      color: #ffffff;
   }
</style>
````

<!-- Buttons -->

<button class="px-4 py-2 bg-accent text-white rounded text-sm font-medium hover:bg-accent/80 transition-colors">Button Text</button>

````

### Stat Cards

```html
<!-- Statistics display cards -->
<div class="bg-white/[0.02] border border-white/5 rounded-lg p-4 flex flex-col items-center">
   <span class="block text-xs text-secondary/80 mb-1 uppercase tracking-wide">Label</span>
   <span class="text-2xl font-bold text-accent">Value</span>
</div>
````

### Status Badges

```html
<!-- Success status -->
<span class="px-2 py-1 rounded text-xs font-medium bg-green-400/20 text-green-400 border border-green-400/30">Completed</span>

<!-- Warning status -->
<span class="px-2 py-1 rounded text-xs font-medium bg-yellow-400/20 text-yellow-400 border border-yellow-400/30">In Progress</span>

<!-- Error status -->
<span class="px-2 py-1 rounded text-xs font-medium bg-red-400/20 text-red-400 border border-red-400/30">Failed</span>
```

### Info Notes

```html
<!-- Info note template - Use for all helper text and informational messages -->
<div class="mt-4 pt-3 border-t border-white/5">
   <div class="flex items-center text-xs text-secondary/60">
      <svg class="w-3 h-3 mr-1.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
         <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path>
      </svg>
      Your informational message text here
   </div>
</div>
```

---

## ✅ Custom Checkboxes (Random Accent Glow)

### 🎯 Concept

To align with a futuristic or tech-inspired UI, we hide the native checkbox and use a fully custom, animated checkbox system. It supports dynamic **random accent glows**, accessibility, and smooth transitions while maintaining a consistent dark theme.

---

### 🧩 Key Features

- Hides native browser checkbox using `sr-only` for accessibility
- Custom `div` with SVG serves as the checkbox UI
- Uses vibrant HSL color accents on check
- Smooth width + color transition for pill animation
- `peer-focus` styles ensure accessibility focus outlines
- Can be extended to any number of checkbox inputs

---

### 🖼️ HTML Template

```html
<label class="flex items-center cursor-pointer group">
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
         <path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7" />
      </svg>
   </div>
   <span class="ml-2 text-sm text-primary">Email notifications for payouts</span>
</label>

<label class="flex items-center cursor-pointer group mt-4">
   <input type="checkbox" id="checkbox-sms-alerts" class="sr-only peer" />
   <div
      id="colorBox-sms-alerts"
      class="relative w-4 h-4 rounded border border-white/10 bg-black/5 flex items-center justify-center peer-focus:outline-none peer-focus:ring-2 peer-focus:ring-accent peer-focus:ring-offset-2 peer-focus:ring-offset-black/10 peer-checked:w-10 peer-checked:rounded-xl peer-checked:px-2 transition-all duration-300 ease-in-out"
   >
      <svg
         class="h-3 w-3 text-white opacity-0 peer-checked:opacity-100 transition-opacity duration-200"
         fill="none"
         viewBox="0 0 24 24"
         stroke="currentColor"
         stroke-width="3"
      >
         <path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7" />
      </svg>
   </div>
   <span class="ml-2 text-sm text-primary">SMS alerts for critical errors</span>
</label>
```

---

### ⚡ JavaScript Logic (Random Accent Glow)

```js
<script nonce="<%- NONCE %>">
  const checkboxColorCombos = [
    { boxId: 'colorBox-email-notif', checkId: 'checkbox-email-notif' },
    { boxId: 'colorBox-sms-alerts', checkId: 'checkbox-sms-alerts' },
    // Add more checkbox pairs here
  ];

  checkboxColorCombos.forEach(({ boxId, checkId }) => {
    const checkbox = document.getElementById(checkId);
    const box = document.getElementById(boxId);

    if (!checkbox || !box) {
      console.warn(`Missing checkbox or box for: ${checkId}, ${boxId}`);
      return;
    }

    const applyRandomColor = () => {
      if (checkbox.checked) {
        const hue = Math.floor(Math.random() * 360);
        const color = `hsl(${hue}, 90%, 60%)`; // Neon style
        box.style.backgroundColor = color;
        box.style.borderColor = color;
      } else {
        box.style.backgroundColor = 'rgba(0,0,0,0.05)';
        box.style.borderColor = 'rgba(255,255,255,0.1)';
      }
    };

    checkbox.addEventListener('change', applyRandomColor);
    applyRandomColor(); // Apply on page load
  });
</script>
```

---

### 🧪 Use Cases

| Use Case              | Example                          |
| --------------------- | -------------------------------- |
| Notification Toggles  | Email, SMS, App push             |
| Payment Settings      | Auto-withdraw, billing reminders |
| Privacy & Permissions | Consent for data usage, tracking |
| Feature Flags         | Enable beta features, dark mode  |

---

### 🧠 Best Practices

- Always pair `sr-only` input with a focusable and labelled element.
- Keep color contrast high for readability on dark backgrounds.
- Keep transitions smooth but fast (~200–300ms).
- Store checked states in backend/localStorage if needed for persistence.

**Usage Examples:**

- Form field validation info (e.g., error messages, character limits)
- Character limits
- Privacy explanations
- Read-only field descriptions
- Help text and instructions

**Design Features:**

- ✅ Consistent info icon with proper spacing
- ✅ Visual separation with border
- ✅ Muted styling for non-intrusive appearance
- ✅ Dark theme optimized contrast

---

## Toggle Switches

### Compact Toggle Switch

```html
<!-- Compact toggle switch -->
<label class="relative inline-flex items-center cursor-pointer">
   <input type="checkbox" id="uniqueId" class="sr-only peer" />
   <div class="w-9 h-5 bg-gray-600/50 peer-focus:outline-none rounded-full peer-checked:bg-green-500 transition-colors"></div>
</label>
```

### Toggle with Label Structure

```html
<div class="flex items-center justify-between">
   <div>
      <p class="font-medium text-primary">Feature Name</p>
      <p class="text-sm text-secondary/70">Feature description</p>
   </div>
   <label class="relative inline-flex items-center cursor-pointer">
      <input type="checkbox" id="featureToggle" class="sr-only peer" />
      <div class="w-9 h-5 bg-gray-600/50 peer-focus:outline-none rounded-full peer-checked:bg-green-500 transition-colors"></div>
   </label>
</div>
```

### Toggle with Checked State

```html
<label class="relative inline-flex items-center cursor-pointer">
   <input type="checkbox" id="enabledFeature" checked class="sr-only peer" />
   <div class="w-9 h-5 bg-gray-600/50 peer-focus:outline-none rounded-full peer-checked:bg-green-500 transition-colors"></div>
</label>
```

### Toggle Switch Specifications

```css
/* Toggle switch exact dimensions and colors */
.toggle-switch {
   width: 2.25rem; /* w-9 - 36px */
   height: 1.25rem; /* h-5 - 20px */
   background: rgba(75, 85, 99, 0.5); /* bg-gray-600/50 - OFF state */
   border-radius: 9999px; /* rounded-full */
   transition: background-color 0.15s ease-in-out; /* transition-colors */
}

.toggle-switch:checked {
   background: rgb(34, 197, 94); /* peer-checked:bg-green-500 - ON state */
}

/* Focus state */
.toggle-switch:focus {
   outline: none; /* peer-focus:outline-none */
   box-shadow: 0 0 0 2px rgba(34, 197, 94, 0.5); /* Optional focus ring */
}
```

### Toggle Switch Variations

```html
<!-- Basic toggle -->
<label class="relative inline-flex items-center cursor-pointer">
   <input type="checkbox" class="sr-only peer" />
   <div class="w-9 h-5 bg-gray-600/50 peer-focus:outline-none rounded-full peer-checked:bg-green-500 transition-colors"></div>
</label>

<!-- Toggle with notification class -->
<label class="relative inline-flex items-center cursor-pointer">
   <input type="checkbox" class="sr-only peer notification-toggle" />
   <div class="w-9 h-5 bg-gray-600/50 peer-focus:outline-none rounded-full peer-checked:bg-green-500 transition-colors"></div>
</label>

<!-- Toggle with custom ID for JavaScript -->
<label class="relative inline-flex items-center cursor-pointer">
   <input type="checkbox" id="customToggle" class="sr-only peer" />
   <div class="w-9 h-5 bg-gray-600/50 peer-focus:outline-none rounded-full peer-checked:bg-green-500 transition-colors"></div>
</label>

<!-- Disabled toggle -->
<label class="relative inline-flex items-center cursor-not-allowed opacity-50">
   <input type="checkbox" disabled class="sr-only peer" />
   <div class="w-9 h-5 bg-gray-600/50 peer-focus:outline-none rounded-full peer-checked:bg-green-500 transition-colors"></div>
</label>
```

---

## Clean Selection Cards

### Pattern

```html
<!-- Clean selection cards pattern - No visual indicators, border highlight only -->
<div class="selection-container space-y-3">
   <!-- Selected card -->
   <label class="selection-card selected" data-option="option1">
      <input type="checkbox" checked class="selection-checkbox" />
      <div class="card-content">
         <div class="option-info">
            <h4>Option Title</h4>
            <p>Option description or details</p>
         </div>
         <i class="option-icon">🎯</i>
      </div>
   </label>

   <!-- Unselected card -->
   <label class="selection-card" data-option="option2">
      <input type="checkbox" class="selection-checkbox" />
      <div class="card-content">
         <div class="option-info">
            <h4>Another Option</h4>
            <p>Alternative option description</p>
         </div>
         <i class="option-icon">⚡</i>
      </div>
   </label>
</div>
```

### Required CSS

```css
.selection-card {
   display: flex;
   align-items: center;
   padding: 16px;
   background: rgba(255, 255, 255, 0.02);
   border: 1px solid rgba(255, 255, 255, 0.05);
   border-radius: 8px;
   cursor: pointer;
   transition: all 0.3s ease;
   color: white;
}

.selection-card:hover {
   background: rgba(255, 255, 255, 0.08);
}

.selection-card.selected {
   border-color: #06b6d4 !important;
   background: rgba(6, 182, 212, 0.05) !important;
}

.selection-checkbox {
   position: absolute;
   width: 1px;
   height: 1px;
   overflow: hidden;
   clip: rect(0, 0, 0, 0);
}

.card-content {
   display: flex;
   justify-content: space-between;
   align-items: center;
   width: 100%;
}

.option-info h4 {
   margin: 0 0 4px 0;
   font-size: 16px;
   font-weight: 600;
}

.option-info p {
   margin: 0;
   font-size: 14px;
   color: rgba(255, 255, 255, 0.7);
}

.option-icon {
   font-size: 20px;
   opacity: 0.8;
}
```

### JavaScript for Selection Cards

```js
<script>
   document.querySelectorAll('.selection-card').forEach((card) => {
      const checkbox = card.querySelector('.selection-checkbox');

      if (checkbox.checked) card.classList.add('selected');

      card.addEventListener('click', function (e) {
         if (e.target === checkbox) return;

         checkbox.checked = !checkbox.checked;
         card.classList.toggle('selected', checkbox.checked);
      });
   });
</script>
```

### Use Cases

```html
<!-- Payment methods -->
<div class="selection-container space-y-3">
   <label class="selection-card selected" data-payment="razorpay">
      <input type="checkbox" checked class="selection-checkbox" />
      <div class="card-content">
         <div class="option-info">
            <h4>Razorpay</h4>
            <p>Credit/Debit cards, UPI, Net Banking</p>
         </div>
         <i class="option-icon">💳</i>
      </div>
   </label>
</div>

<!-- Notification preferences -->
<div class="selection-container space-y-3">
   <label class="selection-card selected" data-notification="email">
      <input type="checkbox" checked class="selection-checkbox" />
      <div class="card-content">
         <div class="option-info">
            <h4>Email Notifications</h4>
            <p>Get notified via email</p>
         </div>
         <i class="option-icon">📧</i>
      </div>
   </label>
</div>

<!-- Theme selection -->
<div class="selection-container space-y-3">
   <label class="selection-card selected" data-theme="dark">
      <input type="radio" name="theme" checked class="selection-checkbox" />
      <div class="card-content">
         <div class="option-info">
            <h4>Dark Theme</h4>
            <p>Easy on the eyes</p>
         </div>
         <i class="option-icon">🌙</i>
      </div>
   </label>
</div>

<!-- Service plans -->
<div class="selection-container space-y-3">
   <label class="selection-card selected" data-plan="pro">
      <input type="radio" name="plan" checked class="selection-checkbox" />
      <div class="card-content">
         <div class="option-info">
            <h4>Pro Plan</h4>
            <p>$19/month - Advanced features</p>
         </div>
         <i class="option-icon">🚀</i>
      </div>
   </label>
</div>
```

### Design Features

- **No Visual Indicators**: Clean minimal design without checkmarks or round buttons
- **Border Highlight Selection**: Cyan border when selected (`#06b6d4`)
- **Hidden Checkboxes**: Accessible but invisible (`sr-only` pattern)
- **Subtle Hover Effects**: Gentle background change on interaction
- **Dark Theme Optimized**: Perfect contrast ratios for dark backgrounds
- **Flexible Content**: Works with any text, descriptions, and icons
- **Input Type Agnostic**: Supports both `checkbox` and `radio` inputs
- **Mobile Responsive**: Scales appropriately on all devices

### Customization

```css
/* Change accent color */
.selection-card.selected {
   border-color: #your-color !important;
   background: rgba(your-rgb-values, 0.05) !important;
}

/* Light theme variant */
.selection-card {
   background: rgba(0, 0, 0, 0.02);
   border: 1px solid rgba(0, 0, 0, 0.05);
   color: black;
}

.selection-card:hover {
   background: rgba(0, 0, 0, 0.08);
}

/* Mobile responsive adjustments */
@media (max-width: 768px) {
   .selection-card {
      padding: 12px;
   }

   .option-info h4 {
      font-size: 14px;
   }

   .option-info p {
      font-size: 12px;
   }
}
```

---

## 🔔 Notification Components (Toast & Bubble)

These components use the same dark theme system and inherit all color and layout utilities.

---

### Toast Messages

#### Usage

Use toast messages for:

- Temporary notifications
- Status updates (success, error, warning, info)
- Top-right stackable UX

#### HTML Example

```html
<div class="fixed top-4 right-4 z-50 flex flex-col gap-2">
   <!-- Success Toast -->
   <div class="px-4 py-2 rounded-lg text-sm font-medium bg-green-400/20 text-green-400 border border-green-400/30 shadow-lg">
      <div class="flex items-center">
         <svg class="w-4 h-4 mr-2 text-green-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path d="M5 13l4 4L19 7" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
         </svg>
         Stock updated successfully!
      </div>
   </div>
</div>
```

### Mouse Bubble Notification

```css
#mouse-bubble {
   position: fixed;
   z-index: 9999;
   pointer-events: none;
   padding: 4px 8px;
   font-size: 12px;
   border-radius: 6px;
   background: rgba(30, 30, 30, 0.5); /* dark translucent */
   backdrop-filter: blur(8px); /* glassmorphism */
   color: white;
   border: 1px solid rgba(255, 255, 255, 0.15);
   box-shadow: 0 4px 12px rgba(0, 0, 0, 0.4);
   transform: translate(0px, 0px) scale(0.95);
   opacity: 0;
   transition:
      opacity 0.2s ease,
      transform 0.2s ease;
}
```

---

## Why Use Different Colors for Section Bars?

Using different colors for section header bars and metric cards is a key part of this theme's design system. Here’s why this approach is recommended:

- **Visual Hierarchy & Clarity:** Unique colors for each section’s vertical bar make it easy to distinguish between different areas of the dashboard at a glance. This improves scan-ability and helps users quickly find the information they need.
- **Quick Section Identification:** Color-coding allows users to associate a color with a specific topic or section, acting as a visual shortcut and reducing cognitive load.
- **Consistent Theme & Branding:** Using the theme’s approved palette ensures the dashboard remains visually cohesive and professional, reinforcing your brand’s design language.
- **Accessibility:** Color differentiation, when paired with good contrast, helps users with attention or memory challenges, and can aid those with mild color vision deficiencies (as long as colors are distinct and not the only indicator).
- **Modern, Engaging Look:** Colored bars add vibrancy and a tech-inspired feel, aligning with the “cyber/tech-punk” and “minimal” design principles of this theme.

**In summary:**
Using different colors for section bars is not just a stylistic choice—it’s a best practice for clarity, speed, and a delightful user experience, all while maintaining theme consistency and brand identity.

---

## Quick Analytics Cards (with Random Hover Colors)

```html
<!-- Quick Analytics Card Grid -->
<div class="grid grid-cols-1 sm:grid-cols-2 gap-3 sm:gap-4">
   <!-- Example Card -->
   <div
      class="quick-analytics-card flex flex-col bg-black/5 border border-purple-400/20 rounded-lg p-3 transition-colors duration-300 cursor-pointer"
   >
      <span class="text-xs text-secondary/70 mb-1 uppercase tracking-wide">Top Category</span>
      <span class="text-base font-bold text-accent">Fashion</span>
   </div>
   <div class="quick-analytics-card flex flex-col bg-black/5 border border-green-400/20 rounded-lg p-3 transition-colors duration-300 cursor-pointer">
      <span class="text-xs text-secondary/70 mb-1 uppercase tracking-wide">Average Price</span>
      <span class="text-base font-bold text-green-400">₹1,299</span>
   </div>
   <div class="quick-analytics-card flex flex-col bg-black/5 border border-blue-400/20 rounded-lg p-3 transition-colors duration-300 cursor-pointer">
      <span class="text-xs text-secondary/70 mb-1 uppercase tracking-wide">Total Revenue</span>
      <span class="text-base font-bold text-blue-400">₹2,45,000</span>
   </div>
   <div
      class="quick-analytics-card flex flex-col bg-black/5 border border-purple-400/20 rounded-lg p-3 transition-colors duration-300 cursor-pointer"
   >
      <span class="text-xs text-secondary/70 mb-1 uppercase tracking-wide">Best Seller</span>
      <span class="text-base font-bold text-purple-400">Sneaker X</span>
   </div>
</div>
```

```js
<script>
  // Random hover color effect for quick analytics cards
  const quickAnalyticsCards = document.querySelectorAll('.quick-analytics-card');
  const hoverColors = [
    'rgba(139, 92, 246, 0.18)', // purple
    'rgba(34, 197, 94, 0.18)',  // green
    'rgba(59, 130, 246, 0.18)', // blue
    'rgba(6, 182, 212, 0.18)',  // cyan
    'rgba(251, 191, 36, 0.18)', // yellow
    'rgba(239, 68, 68, 0.18)',  // red
    'rgba(168, 85, 247, 0.18)', // violet
    'rgba(236, 72, 153, 0.18)'  // pink
  ];
  quickAnalyticsCards.forEach(card => {
    card.addEventListener('mouseenter', () => {
      const color = hoverColors[Math.floor(Math.random() * hoverColors.length)];
      card.style.backgroundColor = color;
    });
    card.addEventListener('mouseleave', () => {
      card.style.backgroundColor = '';
    });
  });
</script>
```

**Features:**

- Modern grid layout, theme-colored borders, and dark backgrounds
- Each card uses a different border color for quick visual distinction
- On hover, each card animates to a random theme color for a playful, tech-inspired effect
- Responsive and accessible

**Usage:**
Use for dashboard quick stats, analytics, or summary panels. Place inside any card or section for instant theme consistency and interactivity.

---

---

## 🧩 FieldGridPreview

A reusable grid layout for grouped form fields, matching the KawaiiNinja dark theme.
Use for attributes, settings, options, or any multi-field input group.

### Features

- Responsive grid: 1 column on mobile, 4 columns on desktop
- Consistent gap, padding, border, and background
- All fields and buttons use full width
- Supports any field type (text, select, checkbox, toggle, button, etc.)
- Muted/disabled preview mode available

---

### 🖼️ HTML Template

```html
<!-- FieldGridPreview Example -->
<div class="grid grid-cols-1 md:grid-cols-4 gap-2 bg-white/[0.02] border border-white/5 rounded-lg px-3 py-2">
   <!-- Text input -->
   <input type="text" placeholder="Text Field" class="px-2 py-1 rounded-md bg-black/10 border border-white/10 text-primary text-xs w-full" />
   <!-- Select dropdown -->
   <select class="dark-select px-2 py-1 rounded-md bg-black/10 border border-white/10 text-primary text-xs w-full">
      <option>Option 1</option>
      <option>Option 2</option>
   </select>
   <!-- Checkbox -->
   <label class="flex items-center text-xs text-secondary w-full">
      <input type="checkbox" class="mr-2" />
      <span>Checkbox</span>
   </label>
   <!-- Button -->
   <button type="button" class="text-accent text-xs rounded-md px-2 py-1 bg-black/5 border border-white/10 w-full">Action</button>
</div>
```

---

### 🖼️ Disabled/Preview Mode

```html
<!-- FieldGridPreview Disabled Example -->
<div class="grid grid-cols-1 md:grid-cols-4 gap-2 bg-white/[0.02] border border-white/5 rounded-lg px-3 py-2 opacity-60 pointer-events-none">
   <input
      type="text"
      placeholder="Text Field"
      class="px-2 py-1 rounded-md bg-black/10 border border-white/10 text-primary text-xs w-full"
      value="Sample Text"
      disabled
   />
   <select class="dark-select px-2 py-1 rounded-md bg-black/10 border border-white/10 text-primary text-xs w-full" disabled>
      <option>Option 1</option>
   </select>
   <label class="flex items-center text-xs text-secondary w-full">
      <input type="checkbox" class="mr-2" checked disabled />
      <span>Checkbox</span>
   </label>
   <button type="button" class="text-accent text-xs rounded-md px-2 py-1 bg-black/5 border border-white/10 w-full" disabled>Action</button>
</div>
```

```html
Example
<div class="mb-4">
   <label class="block text-xs font-medium text-secondary mb-2">Attributes Dummy</label>
   <div id="attributesContainerDummy" class="space-y-2">
      <div class="grid grid-cols-1 md:grid-cols-4 gap-2 bg-white/[0.02] border border-white/5 rounded-lg px-3 py-2 opacity-60 pointer-events-none">
         <input
            type="text"
            placeholder="Name"
            class="attr-name px-2 py-1 rounded-md bg-black/10 border border-white/10 text-primary text-xs w-full"
            value="Bluetooth Version"
            disabled
         />
         <input
            type="text"
            placeholder="Value"
            class="attr-value px-2 py-1 rounded-md bg-black/10 border border-white/10 text-primary text-xs w-full"
            value="5.0"
            disabled
         />
         <label class="flex items-center text-xs text-secondary w-full">
            <input type="checkbox" class="attr-display" checked disabled />
            <span class="ml-1">Display</span>
         </label>
         <button type="button" class="remove-attr-btn text-red-500 text-xs rounded-md px-2 py-1 bg-black/5 border border-white/10 w-full" disabled>
            Remove
         </button>
      </div>
   </div>
   <button type="button" id="addAttributeBtnDummy" class="mt-2 px-2 py-1 bg-accent text-white rounded text-xs">Add Attribute</button>
   <input type="hidden" id="productAttributesDummy" name="productAttributesDummy" />
</div>
```

---

**Usage:**

- Use `FieldGridPreview` for any grouped field layouts (attributes, settings, options, etc.).
- Swap in any field type as needed.
- For preview/disabled state, add `opacity-60 pointer-events-none` and `disabled` to fields.

---
