# Tailwind CSS @apply Directive Bug with Pseudo-Element Selectors

This repository demonstrates a bug in Tailwind CSS's `@apply` directive where it fails to correctly apply styles when used with pseudo-element selectors (`:before` and `:after`).  This results in unexpected styling or no styling at all.

## Bug Description
When using `@apply` with a class containing a pseudo-element selector, the expected styles are not applied correctly. This is problematic when you try to use the `@apply` directive for maintainability, but the pseudo-element styles are not inherited properly. 

## Reproduction
1. Clone this repository.
2. Open `bug.html` in your browser.
3. Observe the unexpected styling of the button.  The `::before` pseudo-element should add content, but it does not due to this bug. 

## Solution
The provided `solution.html` demonstrates a workaround by applying the styles directly in the element's class without using the `@apply` directive for pseudo-elements.  This demonstrates that the problem lies within the way `@apply` handles pseudo-element selectors and not a general Tailwind configuration issue. 