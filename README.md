<p align="center">
  <img src="assets/readme/spock.jpeg" alt="Logo" width="250" height="auto" />
</p>

<h1 align="center">@appsweet-co/spock-css</h1>

<p align="center">
  <b>Lightweight CSS utilities using logical properties and CSS variables</b></br>
  <sub><sub>
</p>

<br />

Spock CSS is a lightweight CSS utility library. It uses [logical properties](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Logical_Properties) and [CSS Variables](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Variables) to keep things small and easy to work with.

## Quick Start

Install Spock CSS using npm.

```zsh
npm i @appsweet-co/spock-css
```

Import the CSS file as needed.

```css
@import "~@appsweet-co/spock-css/build/spock.min.css";
```

You can also import Spock CSS directly from a CDN.

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@appsweet-co/spock-css@latest/dist/spock.min.css">
  
<!-- OR -->
  
<link rel="stylesheet" href="https://unpkg.com/browse/@appsweet-co/spock-css@latest/dist/spock.min.css">
```

## Design Goals

### Utility First

Utility styles are easy to reuse. They do one thing in the same way every time with no side effects. They keep the [CSS specificity](https://specificity.keegan.st/) flat and eliminate the need to [invent new names](https://en.wikipedia.org/wiki/Principle_of_least_astonishment).

:dart: ***PRO TIP: Read [this article](https://frontstuff.io/in-defense-of-utility-first-css) for more info on why Utility-First CSS is a good thing.***

### Logical Properties

We use [logical properties](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Logical_Properties) instead of traditional directions and dimensions. This makes it easy to localize your projects for right-to-left languages. Example:

```html
<h1 style="--margin-block-end:2rem">Hello World</h1>
```

### CSS Variables

We use [CSS Variables](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Variables) instead of CSS Classes. This keeps our library small and universal.

### Native CSS Functions

We encourage the use of [native CSS functions](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Functions#math_functions) instead of traditional breakpoints like you see in frameworks like [Bootstrap](https://getbootstrap.com/docs/5.1/layout/breakpoints/) or [Tailwind](https://tailwindcss.com/docs/breakpoints). This keeps our library small and makes it easy for your code to work across all screens sizes.

### Theme Agnostic

We make no assumptions about your project's theme. Use CSS variables as needed to set properties. Example:

```html
<h1 style="--color:var(--primary); --font-size:var(--size-lg)">Hello World</h1>
```

We also make no assumptions about your project's baseline CSS. We built our library to work well with other CSS Frameworks like [Bootstrap](https://getbootstrap.com/docs/5.1/layout/breakpoints/) or [Tailwind](https://tailwindcss.com/docs/breakpoints).

### Verbose Names

Abbreviations are hard to understand. Our utility names mirror the selectors they reference. This makes it easy to read and write. Examples:

```html
<div style="--aspect-ratio:1; --width:100vw">
  <h1 style="--text-align:center">Hello World</h1>
</div>
```
