{{ template:logo }}
{{ template:title }}
{{ template:description }}
<!-- {{ template:badges }} -->

Spock CSS is a lightweight CSS utility library. It uses [logical properties](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Logical_Properties) instead of the traditional directions and dimensions. This makes it easy to internationalize your projects. 

## Design Goals

### Utility First

We use [utility classes](https://adamwathan.me/css-utility-classes-and-separation-of-concerns/) and [utility styles](https://www.bonsaicss.com/#style-based-utilities) when possible. Utilities are easy to reuse. They do one thing in the same way every time with no side effects. They keep the [CSS specificity](https://specificity.keegan.st/) flat and eliminate the need to [invent new names](https://en.wikipedia.org/wiki/Principle_of_least_astonishment).

:dart: ***PRO TIP: Read [this article](https://frontstuff.io/in-defense-of-utility-first-css) for more info on why Utility-First CSS is a good thing.***

We use both [class selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/Class_selectors) and variables assigned to the [`style` attribute](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/style).

- CSS Classes _limit_ options to a small number of known values. Options should align with our [generic scale](src/partials/_scale.scss) when possible. Examples: [padding](src/partials/_padding.scss), [text](src/partials/_text.scss).

- CSS Variables _widen_ options to a large number of unknown values. Examples: [aspect-ratio](src/partials/_aspect-ratio.scss), [dimensions](src/partials/_dimensions.scss).

### Logical Properties

We use [logical properties](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Logical_Properties) instead of the traditional directions and dimensions. This makes it easy to localize your projects for right-to-left languages. Example:

```html
<h1 class="padding-inline-md">Hello World</h1>
```

### Native CSS Functions

We encourage the use of [native CSS functions](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Functions#math_functions) instead of traditional breakpoints like you see in frameworks like [Bootstrap](https://getbootstrap.com/docs/5.1/layout/breakpoints/) or [Tailwind](https://tailwindcss.com/docs/breakpoints). This reduces the size of the Spock CSS libaray and makes it easy for your code to work across all screens sizes.

### Theme Agnostic

We make no assumptions about your project's theme. Use CSS variables as needed to set properties. Example:

```html
<h1 style="--color: var(--primary); --font-size:var(--size-lg)">Hello World</h1>
```

### Verbose Names

Abbreviations are hard to grok. Our classes and variables mirror the selectors they reference. This makes it easy to read and write.

## Default Scale

The default scale includes five t-shirt sizes that work well with [8pt grids](https://spec.fm/specifics/8-pt-grid):

```css
:root {
  --spock-scale-xs: 0.5rem;
  --spock-scale-sm: 1.5rem;
  --spock-scale-md: 2.5rem;
  --spock-scale-lg: 3.5rem;
  --spock-scale-xl: 4.5rem;
}
```

Use standard CSS cascade rules to override this scale. 

## Baseline CSS

We make no assumptions about your project's baseline CSS. Manually reset properties or use a [CSS Reset tool](http://meyerweb.com/eric/tools/css/reset/) as needed.

## Available Utilities 

_As of v{{ pkg.version }}_

### Classes

- `.box-sizing-border-box`
- `.box-sizing-content-box`
- `.display-block`
- `.display-contents`
- `.display-flex`
- `.display-grid`
- `.display-inline`
- `.display-inline-block`
- `.display-inline-flex`
- `.display-inline-grid`
- `.display-none`
- `.font-weight-100`
- `.font-weight-200`
- `.font-weight-300`
- `.font-weight-400`
- `.font-weight-500`
- `.font-weight-600`
- `.font-weight-700`
- `.font-weight-800`
- `.font-weight-900`
- `.font-weight-bold`
- `.font-weight-bolder`
- `.font-weight-lighter`
- `.font-weight-normal`
- `.inset-0`
- `.inset-block-0`
- `.inset-block-end-lg`
- `.inset-block-end-md`
- `.inset-block-end-sm`
- `.inset-block-end-xl`
- `.inset-block-end-xs`
- `.inset-block-lg`
- `.inset-block-md`
- `.inset-block-sm`
- `.inset-block-start-lg`
- `.inset-block-start-md`
- `.inset-block-start-sm`
- `.inset-block-start-xl`
- `.inset-block-start-xs`
- `.inset-block-xl`
- `.inset-block-xs`
- `.inset-inline-0`
- `.inset-inline-end-lg`
- `.inset-inline-end-md `
- `.inset-inline-end-sm `
- `.inset-inline-end-xl`
- `.inset-inline-end-xs `
- `.inset-inline-lg `
- `.inset-inline-md `
- `.inset-inline-sm `
- `.inset-inline-start-lg `
- `.inset-inline-start-md `
- `.inset-inline-start-sm `
- `.inset-inline-start-xl`
- `.inset-inline-start-xs `
- `.inset-inline-xl`
- `.inset-inline-xs `
- `.margin-0`
- `.margin-block-0`
- `.margin-block-end-lg`
- `.margin-block-end-md`
- `.margin-block-end-sm`
- `.margin-block-end-xl`
- `.margin-block-end-xs`
- `.margin-block-lg`
- `.margin-block-md`
- `.margin-block-sm`
- `.margin-block-start-lg`
- `.margin-block-start-md`
- `.margin-block-start-sm`
- `.margin-block-start-xl`
- `.margin-block-start-xs`
- `.margin-block-xl`
- `.margin-block-xs`
- `.margin-inline-0`
- `.margin-inline-end-lg`
- `.margin-inline-end-md`
- `.margin-inline-end-sm`
- `.margin-inline-end-xl`
- `.margin-inline-end-xs`
- `.margin-inline-lg`
- `.margin-inline-md`
- `.margin-inline-sm`
- `.margin-inline-start-lg`
- `.margin-inline-start-md`
- `.margin-inline-start-sm`
- `.margin-inline-start-xl`
- `.margin-inline-start-xs`
- `.margin-inline-xl`
- `.margin-inline-xs`
- `.padding-0`
- `.padding-block-0`
- `.padding-block-end-lg`
- `.padding-block-end-md`
- `.padding-block-end-sm`
- `.padding-block-end-xl`
- `.padding-block-end-xs`
- `.padding-block-lg`
- `.padding-block-md`
- `.padding-block-sm`
- `.padding-block-start-lg`
- `.padding-block-start-md`
- `.padding-block-start-sm`
- `.padding-block-start-xl`
- `.padding-block-start-xs`
- `.padding-block-xl`
- `.padding-block-xs`
- `.padding-inline-0`
- `.padding-inline-end-lg`
- `.padding-inline-end-md`
- `.padding-inline-end-sm`
- `.padding-inline-end-xl`
- `.padding-inline-end-xs`
- `.padding-inline-lg`
- `.padding-inline-md`
- `.padding-inline-sm`
- `.padding-inline-start-lg`
- `.padding-inline-start-md`
- `.padding-inline-start-sm`
- `.padding-inline-start-xl`
- `.padding-inline-start-xs`
- `.padding-inline-xl`
- `.padding-inline-xs`
- `.position-absolute`
- `.position-fixed`
- `.position-relative`
- `.position-static`
- `.position-sticky`
- `.text-align-center`
- `.text-align-end`
- `.text-align-justify`
- `.text-align-start`

### Variables

- `--aspect-ratio`
- `--background-color`
- `--block-size`
- `--border`
- `--border-block`
- `--border-block-end`
- `--border-block-start`
- `--border-end-end-radius`
- `--border-end-start-radius`
- `--border-inline`
- `--border-inline-end`
- `--border-inline-start`
- `--border-radius`
- `--border-start-end-radius`
- `--border-start-start-radius`
- `--color`
- `--font-size`
- `--inline-size`
- `--inset`
- `--inset-block`
- `--inset-block-end`
- `--inset-block-start`
- `--inset-inline`
- `--inset-inline-end`
- `--inset-inline-start`
- `--margin`
- `--margin-block`
- `--margin-block-end`
- `--margin-block-start`
- `--margin-inline`
- `--margin-inline-end`
- `--margin-inline-start`
- `--max-block-size`
- `--max-inline-size`
- `--min-block-size`
- `--min-inline-size`
- `--padding`
- `--padding-block`
- `--padding-block-end`
- `--padding-block-start`
- `--padding-inline`
- `--padding-inline-end`
- `--padding-inline-start`
- `--spock-scale-lg`
- `--spock-scale-md`
- `--spock-scale-sm`
- `--spock-scale-xl`
- `--spock-scale-xs`

## Updating This README

We generate this README with the [@appnest/readme](https://github.com/andreasbm/readme) tool.

Run `npx @appnest/readme generate` or `npm run readme` to update this file.
