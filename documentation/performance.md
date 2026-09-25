# Performance

Repose has no build step: Shopify serves the theme's files directly, and the
theme is built to load quickly by default, using responsive images sized to
where they're actually displayed, lazy loading for anything below the fold,
deferred scripts, and Shopify's Section Rendering API for cart and filter
updates, so those don't reload the whole page. Out of the box, on a store
with real content and no heavy customisation, this is close to as fast as
the theme gets.

Most of what affects performance from here on is in your hands: what you add
to the theme, not the theme itself.

## What affects your store's speed most

1. **Image size and count.** This is the single biggest factor in most
   stores. Upload appropriately sized source images (see
   [Images and video](images-and-video.md)) and avoid sections packed with
   more large images than a page needs.
2. **Apps.** Every app you install can add its own scripts, stylesheets and
   network requests, largely outside the theme's control. Remove apps you've
   stopped using rather than just disabling their embed, and prefer apps
   that load only where they're needed rather than on every page.
3. **Custom Liquid and tracking code.** The Custom Liquid section and block,
   and the custom head/body code slots in
   [Theme settings > SEO and tracking](theme-settings.md#seo-and-tracking),
   run exactly what you paste into them. Keep them minimal, and remove
   anything you're not actively using.
4. **Fonts.** Choosing web fonts for all four font roles (rather than a
   system font for one or more) adds a download for each variant loaded.
   This is a reasonable trade for brand fit, but is worth knowing if you're
   chasing the fastest possible load.
5. **Section and block count on a single page.** A very long homepage with
   many heavy sections stacked one after another will always be slower than
   a focused one, regardless of theme.

## Animation

The **Motion** settings in Theme settings let you turn off reveal animations
and product-card image zoom entirely if you'd rather not have them, though
neither is a significant performance cost on its own; both animate only
transform and opacity, and respect a visitor's reduced-motion preference
automatically. See [Theme settings](theme-settings.md#motion).

## Checking your store's performance

Use a real, published page with your actual content, not an empty preview,
when checking performance: Google's PageSpeed Insights or the Lighthouse
panel in Chrome DevTools are the standard tools for this. Always check on a
browser without an active Shopify admin session, since an admin session
previews your unpublished development theme rather than what a visitor
actually receives, which can look identical while being an entirely
different page.
