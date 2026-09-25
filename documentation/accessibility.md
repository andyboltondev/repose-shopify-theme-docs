# Accessibility

Repose is built to a set of accessibility standards from the ground up, and
those hold regardless of which preset or settings you choose. This page
covers what the theme handles for you automatically, and where the result
still depends on choices you make.

## What the theme handles

- **Full keyboard access.** Every interactive element, including dropdown
  and mega menus, the mobile menu, the cart drawer, dialogs, and the product
  gallery, can be reached and operated with a keyboard alone, with a visible
  focus outline at every stop.
- **Dialogs behave correctly.** The search dialog, cart drawer and minicart,
  and the product image lightbox all trap focus while open, return focus to
  whatever opened them when closed, and close on <kbd>Escape</kbd>.
- **Live updates are announced.** Cart changes (adding, updating or removing
  an item) and filter changes on collection and search pages are announced
  to screen readers through a live region, not just shown visually.
- **Colour contrast.** Every default colour pairing in both the light and
  dark palettes, and every accent use (buttons, links, badges, focus
  rings), meets 4.5:1 contrast for body text and 3:1 for large text, borders
  and icons.
- **Structural correctness.** Headings run in visually distinct, logical
  order; form fields have proper labels linked by ID; focus order follows
  the visual order of the page; touch targets are at least 24 by 24 CSS
  pixels.
- **Motion respects preference.** All animation, including the optional
  reveal animations and image zoom, is disabled automatically for visitors
  whose operating system requests reduced motion, regardless of the Motion
  settings.

## What's still yours to get right

- **Image alt text.** The theme renders whatever alt text you write for
  each image in Shopify admin; it cannot generate a meaningful description
  for you. Write real, descriptive alt text for every product, collection
  and content image. If you use the [variant image grouping
  rules](products-and-collections.md#variant-image-grouping), write the
  actual description first and add the matching rules after it, not instead
  of it.
- **Custom colours.** If you move away from a preset's default palette,
  re-check contrast yourself, particularly for your primary and secondary
  action colours, which are used for buttons, links and focus indicators
  throughout the site. A colour picker's preview doesn't check contrast for
  you.
- **Custom Liquid and app blocks.** Content added through the Custom Liquid
  section or block, or through third-party app blocks, is outside the
  theme's control. Keyboard access, focus handling and contrast for that
  content are the responsibility of whoever wrote it.
- **Video and audio.** If you add video with spoken content, captions are
  your responsibility to provide, typically through the video's own hosting
  platform.
- **Long-form content.** Rich text, blog articles and page content should
  still follow good practice on your end: meaningful link text (not "click
  here"), a sensible heading structure within the content, and alt text on
  any images you insert into a rich text field.

## A note on testing

Automated accessibility checkers (including Google Lighthouse) catch a
meaningful subset of issues but not everything; they're a good first pass,
not a substitute for checking with a keyboard and, where possible, a screen
reader. If something in the theme itself doesn't behave as described above,
that's a bug: see [Troubleshooting](troubleshooting.md) for how to report
it.
