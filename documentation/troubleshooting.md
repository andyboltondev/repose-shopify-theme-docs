# Troubleshooting

## Star ratings aren't showing on a product

The rating block and card ratings read the standard `reviews.rating` and
`reviews.rating_count` metafields, and show nothing at all when either is
missing. Shopify's own free Product Reviews app has been discontinued, so
you'll need a third-party review app that writes to those same reserved
metafields, and reviews need to exist on that product before a rating
appears. See [Products and collections](products-and-collections.md#ratings).

## "Complementary products" recommendations are empty or look unrelated

Complementary recommendations come from pairings you curate per product in
Shopify's free Search & Discovery app, not from automatic matching. Until
you've set pairings for a product there, the recommendations section shows
nothing for it. If you'd rather have automatic matching with no setup,
switch the section's **Recommendation type** to **Related products**
instead. See
[Products and collections](products-and-collections.md#product-recommendations).

## The mega menu isn't appearing, just a regular dropdown

The wider mega menu layout only appears when a menu item has three levels:
a top-level item, with children, at least one of which also has its own
children. Two levels always shows as a regular dropdown. Check your menu
structure under **Online Store > Navigation**. See
[Navigation and menus](navigation-and-menus.md#menu-depth-and-the-mega-menu).

## The country or language selector isn't showing in the footer

Both selectors are on by default in the footer section, but each only
renders when your store actually has more than one option to choose from:
more than one market enabled in **Settings > Markets** for the country
selector, and more than one published language in **Settings > Languages**
for the language selector. A single-market, single-language store won't
show either, even with the setting turned on.

## Colours or the logo look wrong in dark mode

Check that you've defined a full dark palette under
[Theme settings > Dark colour palette](theme-settings.md#light-colour-palette--dark-colour-palette),
separate from the light one; a colour left at a light-mode-appropriate value
there will carry into dark mode as-is. If your logo doesn't read well on a
dark background, add a dedicated dark-mode logo under
[Theme settings > Brand](theme-settings.md#brand) rather than relying on the
same file for both.

## An image is cropped in a way that cuts off the subject

Set the image's focal point in Shopify admin (open the image, then **Edit
focal point**) so the theme knows what to keep in frame when cropping for a
narrower space. The hero section additionally has its own manual focal
position controls, separate from the image's own focal point, if you need
more specific control there. See
[Images and video](images-and-video.md#focal-points).

## An alternate template isn't showing up as an option

Alternate templates are chosen per item, not enabled globally. Open the
specific product, collection or page in Shopify admin, and look for the
**Theme template** panel on the right-hand side to choose an alternate
layout. See
[Products and collections](products-and-collections.md#alternate-templates).

## Custom Liquid or custom tracking code broke part of the page

Remove or comment out the code you added in the Custom Liquid section or
block, or in the custom head/body code slots under
[Theme settings > SEO and tracking](theme-settings.md#seo-and-tracking), and
reintroduce it in smaller pieces to isolate the problem. These slots run
exactly what's pasted into them with no validation, so a stray tag or script
error there can affect the rest of the page.

## A setting isn't visible when a store preview looks different from what I published

An admin-authenticated browser session previews your store's unpublished
development theme, not necessarily the live storefront a visitor sees, and
this can look identical to the real thing while being an entirely different
page. Check what visitors actually see in a private or logged-out browser
window, and confirm which theme is published under
**Online Store > Themes**.

## Still stuck

[Open an issue](https://github.com/andyboltondev/repose-shopify-theme-docs/issues/new/choose)
with your theme version (**Online Store > Themes**, next to the theme name)
and a link to the page where the problem is visible. If your store is
password protected, include the password so the page can be reached. Don't
include order details, customer information or admin credentials; issues
here are public.
