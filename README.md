# FibGrid

A CSS Grid layout system built on the Golden Ratio (φ = 1.618).

Columns and rows are divided using recursive φ subdivision, producing seven named cells (A–G) that feel naturally proportioned.

```
61.8%  →  1/φ
23.6%  →  (1 − 1/φ) × 1/φ
 9.0%  →  (1 − 1/φ)² × 1/φ
 5.6%  →  remainder
```

## Usage

1. Add `fibgrid.css` to your project
2. Drop the markup in:

```html
<link rel="stylesheet" href="fibgrid.css">

<div class="fibgrid">
  <div class="fibgrid-cell a">...</div>
  <div class="fibgrid-cell b">...</div>
  <div class="fibgrid-cell c">...</div>
  <div class="fibgrid-cell d">...</div>
  <div class="fibgrid-cell e">...</div>
  <div class="fibgrid-cell f">...</div>
  <div class="fibgrid-cell g">...</div>
</div>
```

## Customisation

Override these CSS custom properties on `.fibgrid`:

| Property | Default | Description |
|---|---|---|
| `--fibgrid-height` | `100vh` | Height of the grid |
| `--fibgrid-gap` | `0px` | Gap between cells |

```css
.fibgrid {
  --fibgrid-height: 600px;
  --fibgrid-gap: 8px;
}
```