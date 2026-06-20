# ease-hover-border-draw

## What does it do?
Border draws itself around an element on hover — top, right, bottom, left in sequence — using `::before` and `::after` pseudo-elements — pure CSS, no JavaScript.

## Features
- `::before` draws top and right borders
- `::after` draws bottom and left borders
- Sequential animation via transition delays
- Custom properties for color and speed

## Usage
```css
.element::before {
  /* top + right borders */
  transition:
    width 0.3s ease,
    height 0.3s ease 0.3s;
}

.element::after {
  /* bottom + left borders */
  transition:
    width 0.3s ease 0.6s,
    height 0.3s ease 0.3s;
}

.element:hover::before,
.element:hover::after {
  width: 100%;
  height: 100%;
}
```

## Customisation
| Variable | Default | Description |
|----------|---------|-------------|
| `--ease-border-draw-color` | `#a78bfa` | Border color |
| `--ease-border-draw-speed` | `0.3s` | Duration per edge |

## Browser Support
- `::before`/`::after` + `transition` — Chrome 26+, Firefox 16+, Safari 6.1+

## Tech Stack
- HTML + CSS only, no JavaScript

## Preview
Open `demo.html` directly in browser.
