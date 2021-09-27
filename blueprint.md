{{ template:logo }}
{{ template:title }}
{{ template:description }}
{{ template:badges }}

Spock CSS is a lightweight CSS utility library. It uses [logical properties](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Logical_Properties) instead of the traditional directions and dimensions. This makes it easy to internationalize your projects. 

## Design Goals

### Utility First

We use [utility classes](https://adamwathan.me/css-utility-classes-and-separation-of-concerns/) and [utility styles](https://www.bonsaicss.com/#style-based-utilities) when possible. Utilities are easy to reuse. They do one thing in the same way every time with no side effects. They keep the [CSS specificity](https://specificity.keegan.st/) flat and also eliminate the need to [invent new names](https://en.wikipedia.org/wiki/Principle_of_least_astonishment).

:dart: ***PRO TIP: Read [this article](https://frontstuff.io/in-defense-of-utility-first-css) for more info on why Utility-First CSS is a good thing.***

We use both [class selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/Class_selectors) and variables assigned to the [`style` attribute](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/style).

- CSS Classes _limit_ options to a small number of known values. Options should align with our [generic scale](src/theme/utility/_scale.scss) when possible. Examples: [padding](src/theme/utility/_padding.scss), [text](src/theme/utility/_text.scss).

- CSS Variables _widen_ options to a large number of unknown values. Examples: [aspect-ratio](src/theme/utility/_aspect-ratio.scss), [dimensions](src/theme/utility/_dimensions.scss).

### Logical Properties

We use [logical properties](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Logical_Properties) instead of the traditional directions and dimensions. This makes it easy to localize your projects for right-to-left languages. Example:

```html
<h1 class="padding-inline-md">Hello World</h1>
```

### Native CSS Functions

We encourage the use of [native CSS functions](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Functions#math_functions) instead of traditional breakpoints like you see in frameworks like [Bootstrap](https://getbootstrap.com/docs/5.1/layout/breakpoints/) or [Tailwind](https://tailwindcss.com/docs/breakpoints). This reduces the size of the Spock CSS libaray and makes it easy for your code to work across all screens sizes.

### Theme Agnostic

We make no assumptions about your project's theme. Use our CSS Variables as needed to set your theme. Example:

```html
<h1 style="--color: var(--primary)">Hello World</h1>
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

## CSS Reset

We use [Eric Meyer's CSS Reset](src/partials/_reset.scss) to reduce inconsistencies between browsers.

## Updating This README

We generate this README with the [@appnest/readme](https://github.com/andreasbm/readme) tool.

Run `npx @appnest/readme generate` or `npm run readme` to update this file.
