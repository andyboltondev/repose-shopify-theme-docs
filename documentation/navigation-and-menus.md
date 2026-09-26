# Navigation and menus

## Header

The header section holds your logo, main menu, and a set of action icons.
Its settings:

| Setting | What it does |
| --- | --- |
| Menu | Which Shopify navigation menu to display. Build or edit this menu under **Online Store > Navigation**. |
| Enable sticky header | Keeps the header visible while a visitor scrolls down the page. |
| Show search | Adds a search icon that opens a search dialog. |
| Show account link | Adds an account icon, shown only when customer accounts are enabled in **Settings > Customer accounts**. |
| Cart icon action | What clicking the cart icon does: open a full cart drawer, open a small minicart popup, or go straight to the cart page. |

### Menu depth and the mega menu

The main menu supports up to three levels. A top-level item with children
shows a dropdown. If any of those children has its own children (a third
level), the dropdown automatically switches to a wider mega menu layout,
grouping each second-level item as a small heading with its own list of
links beneath it. Build this structure in **Online Store > Navigation**
by nesting menu items; the layout follows automatically from how deep the
menu goes, no separate setting required.

### Mobile menu

On narrow screens, the header collapses to a menu button that opens a full
mobile navigation panel, with the same nested structure as the desktop menu
presented as expandable sections. The panel also includes account and cart
links at the bottom, matching what's enabled in the header settings.

### Search

When **Show search** is on, the search icon opens a dialog with a single
search field, submitting to Shopify's native storefront search. Search
results respect the same filtering and sorting settings as collection pages;
see [Products and collections](products-and-collections.md#search-results).

### Colour mode switcher

If **Show light and dark mode switcher** is on in
[Theme settings](theme-settings.md#colour-mode), a sun/moon toggle appears in
the header alongside the other icons.

## The cart

The **Cart icon action** setting on the header controls how customers reach
their cart:

- **Open cart drawer**: a full-height panel slides in, showing every item
  in the cart.
- **Open minicart popup**: a smaller popup showing a preview of the first
  few items, useful for stores that want a lighter-weight confirmation
  rather than a full cart view.
- **Go to cart page**: the icon links directly to the cart page instead of
  opening a popup.

Both the drawer and minicart let customers adjust quantities and remove
items without leaving the page, using Shopify's Section Rendering API, so
updates happen without a full page reload. They also suggest complementary
products once you've set up pairings; see
[Products and collections](products-and-collections.md#product-recommendations). The full **Basket** page (used
when **Go to cart page** is selected, or reached via "view cart" from the
drawer or minicart) has its own section with settings to show the vendor on
each line item and to show an order note field. Accelerated checkout buttons
and the free delivery progress bar in the cart are controlled from
[Theme settings > Basket and checkout](theme-settings.md#basket-and-checkout).

## Footer

The footer section includes your store description (or Shopify's store
description if left blank), social links, and up to 4 additional blocks:
**Menu** (a heading and a Shopify navigation menu) or **Text** (a heading and
rich text), useful for opening hours, contact details, or extra link groups.

| Setting | What it does |
| --- | --- |
| Brand description | Rich text shown under your logo. Falls back to your store's description from **Settings > General** if left blank. |
| Show social links | Shows icons for whichever profiles are filled in under [Theme settings > Social media](theme-settings.md#social-media). |
| Show country/region selector | A dropdown for switching between the countries or regions your store sells to. Only appears when your store has more than one enabled in **Settings > Markets**. |
| Show language selector | A dropdown for switching between storefront languages. Only appears when your store has more than one published language in **Settings > Languages**. |
| Show payment icons | Shows icons for the payment methods enabled in your store. |
| Show policy links | Links to whichever store policies you've published in **Settings > Policies** (refund, privacy, terms, and so on). |

## Breadcrumbs

Product, collection, blog, article and page templates show a breadcrumb trail
back to the home page automatically (for example, Home > Collection name >
Product name). The home page itself has no breadcrumb, since it's the root.
There's no setting to configure this; it follows the page you're on.

## Sitemap section

For a simple, in-page index of your store separate from breadcrumbs and the
header menu, add the **Sitemap** section to a page. See
[Sections and blocks](sections-and-blocks.md#sitemap) for what it includes.
