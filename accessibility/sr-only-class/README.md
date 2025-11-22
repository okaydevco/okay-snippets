# Screen reader only class
## Usage
```html
<!-- ✅ Example of correct usage: place the sr-only text inside the element, not on the interactive element itself -->
<button>
  <svg>[...]</svg>
  <span class="sr-only">Open navigation</span>
</button>

<!-- ❌ Example of incorrect usage: the interactive element itself shouldn't be visually hidden -->
<button class="sr-only">
  <svg>[...]</svg>
  <span>Open navigation</span>
</button>
```

Use the `sr-only` class when an element needs descriptive text that shouldn’t be visible, and no other semantic method is appropriate.

For example, adding a `<title>` to the SVG could also provide accessible text, but titles should describe the graphic—not an action like “Open navigation”. Also be aware that SVG titles show as hover tooltips, which probably is not what you want in this case.

Order in which browsers determine accessible names:
1. `aria-labelledby`
2. `aria-label`
3. HTML attributes like `alt` or `title`
4. From another linked HTML element like `label` or `legend`
5. HTML content

**Order that you should actually follow to implement accessible names:**
1. HTML content
2. HTML attribute or linked element
3. `aria-labelledby`
4. `aria-label`

## References:
- https://developer.mozilla.org/en-US/docs/Glossary/Accessible_name
- https://www.w3.org/WAI/ARIA/apg/practices/names-and-descriptions/
