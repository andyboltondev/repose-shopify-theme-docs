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

## The Sign in with Shop button isn't on the login page

The button comes from Shopify, not the theme. You need the **Shop** sales
channel installed and Shop Pay activated in **Settings > Payments**, and the
**Sign in with Shop** app block added to the login (and registration) page
in the theme editor. Also check that **Account sign-in** in
[Theme settings > Customer accounts](theme-settings.md#customer-accounts) is
set to **Sign in with Shop**. See
[Customer accounts](navigation-and-menus.md#customer-accounts).

## There's no account icon in the header

The icon needs customer accounts turned on in **Settings > Customer
accounts** in Shopify admin, and **Show account link** on in the Header
section. See [Customer accounts](navigation-and-menus.md#customer-accounts).

## Search suggestions aren't appearing as I type

Check that **Enable predictive search** is on in
[Theme settings > Search](theme-settings.md#search). Suggestions only appear
once the shopper has typed a word that matches something in your store.

## The size guide link isn't showing on a product

The **Size chart** block only appears on products that have an option with
"size" in its name (Size, Ring size, Shoe size and so on). Check that the product has such an
option, and that the block is in your product template. If the pop-up opens
but is empty, fill in the block's **Content** or **Page**. See
[Size chart](products-and-collections.md#size-chart).

## The "Only a few left in stock" message isn't showing

It appears only when the **Show a low stock counter** setting is on in the
product's **Price** block, Shopify is tracking inventory for that variant
(**Track quantity** on the variant), and the quantity left is at or below the
**Low stock threshold**. Products that are well stocked, or that don't track
inventory, never show it. See
[Low stock counter](products-and-collections.md#low-stock-counter).

## "Recently viewed" isn't showing any products

The section is hidden until a visitor has looked at at least one other
product, and it only remembers products in that one browser. Visit two
products in a normal browser window and then a third, and the first two
should appear. Private windows and cleared browser data start from empty.
See [Recently viewed products](products-and-collections.md#recently-viewed-products).

## The quick view eye button isn't on product cards

Turn on **Enable quick view** in
[Theme settings > Cards](theme-settings.md#cards). See
[Quick view](products-and-collections.md#quick-view).

## The collection shows numbered pages instead of loading more automatically

**Load more products automatically while scrolling** is a setting on the
Collection products section, and is separate for the search results page,
which always uses numbered pages. Numbered pages are also what shoppers see
when JavaScript is turned off. See
[Infinite scroll](products-and-collections.md#infinite-scroll).

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
