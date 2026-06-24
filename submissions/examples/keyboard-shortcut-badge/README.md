# Keyboard Shortcut Badge Component

## Overview

Keyboard Shortcut Badge is a modern CSS component for displaying keyboard shortcuts with beautiful styling. It resembles shortcut badges found in applications like VS Code, GitHub, Notion, Linear, and other professional SaaS products. Built with pure CSS, it offers multiple size variants, dark mode, glassmorphism effects, and color themes.

## Features

- Modern keyboard key styling with realistic appearance
- Support for single keys and key combinations
- Platform-specific shortcuts (Windows/Linux with Ctrl, Mac with ⌘)
- Multiple size variants (sm, default, lg)
- Dark mode and glassmorphism effects
- Color-coded variants (success, warning, danger, info)
- Command palette hint style for search bars
- Responsive design
- Smooth press animations
- Fully accessible with keyboard navigation
- Respects `prefers-reduced-motion` and `prefers-contrast`
- Zero JavaScript required

## Available Classes

- `.ease-kbd` — Individual keyboard key badge.
- `.ease-kbd-group` — Container for key combinations.
- `.ease-kbd-separator` — Visual separator between keys (usually "+").
- `.ease-kbd-command` — Command palette/hint style with left-aligned text and right-aligned shortcuts.

## Size Variants

- `.ease-kbd-sm` — Small, compact keyboard shortcuts.
- `.ease-kbd-lg` — Large, prominent keyboard shortcuts.

## Style Variants

- `.ease-kbd-dark` — Dark theme for use on light backgrounds.
- `.ease-kbd-glass` — Glassmorphism effect with backdrop blur.

## Color Variants

- `.ease-kbd-success` — Green background for confirmations.
- `.ease-kbd-warning` — Amber background for caution.
- `.ease-kbd-danger` — Red background for destructive actions.
- `.ease-kbd-info` — Blue background for information.

## Usage

### Single Key

```html
<kbd class="ease-kbd">Esc</kbd>
```

### Key Combination

```html
<div class="ease-kbd-group">
  <kbd class="ease-kbd">Ctrl</kbd>
  <span class="ease-kbd-separator">+</span>
  <kbd class="ease-kbd">K</kbd>
</div>
```

### Mac Shortcut

```html
<div class="ease-kbd-group">
  <kbd class="ease-kbd">⌘</kbd>
  <span class="ease-kbd-separator">+</span>
  <kbd class="ease-kbd">Shift</kbd>
  <span class="ease-kbd-separator">+</span>
  <kbd class="ease-kbd">P</kbd>
</div>
```

### Small Size

```html
<div class="ease-kbd-group">
  <kbd class="ease-kbd ease-kbd-sm">Ctrl</kbd>
  <span class="ease-kbd-separator">+</span>
  <kbd class="ease-kbd ease-kbd-sm">P</kbd>
</div>
```

### Large Size

```html
<div class="ease-kbd-group">
  <kbd class="ease-kbd ease-kbd-lg">Ctrl</kbd>
  <span class="ease-kbd-separator">+</span>
  <kbd class="ease-kbd ease-kbd-lg">Enter</kbd>
</div>
```

### Dark Theme

```html
<div class="ease-kbd-group">
  <kbd class="ease-kbd ease-kbd-dark">⌘</kbd>
  <span class="ease-kbd-separator">+</span>
  <kbd class="ease-kbd ease-kbd-dark">K</kbd>
</div>
```

### Glassmorphism

```html
<div class="ease-kbd-group">
  <kbd class="ease-kbd ease-kbd-glass">Ctrl</kbd>
  <span class="ease-kbd-separator">+</span>
  <kbd class="ease-kbd ease-kbd-glass">Shift</kbd>
  <span class="ease-kbd-separator">+</span>
  <kbd class="ease-kbd ease-kbd-glass">A</kbd>
</div>
```

### Command Palette

```html
<div class="ease-kbd-command">
  <span>Search files...</span>
  <div class="ease-kbd-group">
    <kbd class="ease-kbd">Ctrl</kbd>
    <span class="ease-kbd-separator">+</span>
    <kbd class="ease-kbd">P</kbd>
  </div>
</div>
```

### Color Variants

```html
<!-- Success -->
<div class="ease-kbd-group">
  <kbd class="ease-kbd ease-kbd-success">✓</kbd>
  <span class="ease-kbd-separator">+</span>
  <kbd class="ease-kbd ease-kbd-success">Enter</kbd>
</div>

<!-- Warning -->
<div class="ease-kbd-group">
  <kbd class="ease-kbd ease-kbd-warning">!</kbd>
  <span class="ease-kbd-separator">+</span>
  <kbd class="ease-kbd ease-kbd-warning">Delete</kbd>
</div>

<!-- Danger -->
<div class="ease-kbd-group">
  <kbd class="ease-kbd ease-kbd-danger">✕</kbd>
  <span class="ease-kbd-separator">+</span>
  <kbd class="ease-kbd ease-kbd-danger">Esc</kbd>
</div>

<!-- Info -->
<div class="ease-kbd-group">
  <kbd class="ease-kbd ease-kbd-info">?</kbd>
  <span class="ease-kbd-separator">+</span>
  <kbd class="ease-kbd ease-kbd-info">Help</kbd>
</div>
```

### In Documentation

```html
<p>
  Press <div class="ease-kbd-group" style="display: inline-flex;">
    <kbd class="ease-kbd">Ctrl</kbd>
    <span class="ease-kbd-separator">+</span>
    <kbd class="ease-kbd">Shift</kbd>
    <span class="ease-kbd-separator">+</span>
    <kbd class="ease-kbd">P</kbd>
  </div> to open the command palette.
</p>
```

## Customization

Override CSS variables to customize appearance:

```css
.ease-kbd {
  --ease-kbd-bg: #f3f4f6;
  --ease-kbd-color: #111827;
  --ease-kbd-border: #d1d5db;
  --ease-kbd-shadow: 0 2px 6px rgba(15, 23, 42, 0.08), inset 0 1px 0 rgba(255, 255, 255, 0.6);
  --ease-kbd-radius: 0.45rem;
  --ease-kbd-padding: 0.35rem 0.55rem;
  --ease-kbd-gap: 0.35rem;
  --ease-kbd-transition: 0.18s cubic-bezier(0.22, 1, 0.36, 1);
  --ease-kbd-font-size: 0.82rem;
  --ease-kbd-font-weight: 500;
  --ease-kbd-font-family: 'SF Mono', Monaco, 'Cascadia Code', 'Roboto Mono', Consolas, 'Courier New', monospace;
}
```

## Browser Compatibility

- Chrome / Edge (Latest)
- Firefox (Latest)
- Safari (Latest)
- Mobile browsers

## Accessibility

- Native `<kbd>` HTML element for semantic structure.
- Focus-visible styles with clear outline.
- Respects `prefers-reduced-motion` by disabling animations.
- Respects `prefers-contrast` for enhanced border and font weight.
- High contrast color ratios for readability.
- Keyboard-friendly interactive variant.

## Notes

- Use actual keyboard symbols for Mac keys: ⌘ (Command), ⌥ (Option/Alt), ⌫ (Backspace), ↵ (Enter).
- The component is decorative; no JavaScript interactions are included.
- Combine multiple `.ease-kbd` elements within `.ease-kbd-group` for multi-key shortcuts.
- Use `.ease-kbd-separator` with "+" or arrow symbols to show progression.
- The component works inline with text for documentation and hover hints.
