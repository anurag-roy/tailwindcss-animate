# Animation Duration

> Utilities for controlling the duration of CSS animations.

| Class                | Properties                    |
| -------------------- | ----------------------------- |
| `anim-duration-75`   | `animation-duration: 75ms;`   |
| `anim-duration-100`  | `animation-duration: 100ms;`  |
| `anim-duration-150`  | `animation-duration: 150ms;`  |
| `anim-duration-200`  | `animation-duration: 200ms;`  |
| `anim-duration-300`  | `animation-duration: 300ms;`  |
| `anim-duration-500`  | `animation-duration: 500ms;`  |
| `anim-duration-700`  | `animation-duration: 700ms;`  |
| `anim-duration-1000` | `animation-duration: 1000ms;` |

## Basic Usage

### Changing animation duration

Use the `anim-duration-{amount}` utilities to control an element’s `animation-duration`.

```html
<button class="animate-bounce anim-duration-150 ...">Button A</button>
<button class="animate-bounce anim-duration-300 ...">Button B</button>
<button class="animate-bounce anim-duration-700 ...">Button C</button>
```

## Applying Conditionally

### Hover, focus, and other states

Tailwind lets you conditionally apply utility classes in different states using variant modifiers. For example, use `hover:anim-duration-0` to only apply the `anim-duration-0` utility on hover.

```html
<div class="animate-bounce anim-duration-300 hover:anim-duration-0">
	<!-- ... -->
</div>
```

For a complete list of all available state modifiers, check out the [Hover, Focus, & Other States](https://tailwindcss.com/docs/hover-focus-and-other-states) documentation.

### Breakpoints and media queries

You can also use variant modifiers to target media queries like responsive breakpoints, dark mode, prefers-reduced-motion, and more. For example, use `md:anim-duration-0` to apply the `anim-duration-0` utility at only medium screen sizes and above.

```html
<div class="animate-bounce anim-duration-150 md:anim-duration-0">
	<!-- ... -->
</div>
```

To learn more, check out the documentation on [Responsive Design](https://tailwindcss.com/docs/responsive-design), [Dark Mode](https://tailwindcss.com/docs/dark-mode) and [other media query modifiers](https://tailwindcss.com/docs/hover-focus-and-other-states#media-queries).

## Using custom values

### Customizing your theme

By default, Tailwind provides `animation-duration` utilities for all of the built-in browser keyword options. You can customize these values by editing `theme.animationDuration` or `theme.extend.animationDuration` in your `tailwind.config.js` file.

```js
// @filename tailwind.config.js
module.exports = {
	theme: {
		extend: {
			animationDuration: {
				"2s": "2s",
			},
		},
	},
}
```

Learn more about customizing the default theme in the [theme customization](https://tailwindcss.com/docs/theme#customizing-the-default-theme) documentation.

### Arbitrary values

If you need to use a one-off `animation-duration` value that doesn’t make sense to include in your theme, use square brackets to generate a property on the fly using any arbitrary value.

```html
<div class="anim-duration-[2s]">
	<!-- ... -->
</div>
```

Learn more about arbitrary value support in the [arbitrary values](https://tailwindcss.com/docs/adding-custom-styles#using-arbitrary-values) documentation.
