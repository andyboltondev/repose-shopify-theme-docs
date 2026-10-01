# Navigation and menus

## Header

The header section holds your logo, main menu, and a set of action icons.
Its settings:

| Setting | What it does |
| --- | --- |
| Menu | Which Shopify navigation menu to display. Build or edit this menu under **Online Store > Navigation**. |
| Enable sticky header | Keeps the header visible while a visitor scrolls down the page. |
| Show search | Adds a search icon that opens a search dialog. |
| Show account link | Adds an account icon, shown only when customer accounts are enabled in **Settings > Customer accounts**. What it does when clicked depends on the **Account sign-in** theme setting; see [Customer accounts](#customer-accounts). |
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

**Predictive search.** With **Enable predictive search** on (the default, in
[Theme settings > Search](theme-settings.md#search)), a panel of suggestions
appears under the search field as a shopper types: matching search phrases,
products with their image and price, and any matching collections, pages and
articles. Shoppers can click a suggestion, or move through them with the
up and down arrow keys and press <kbd>Enter</kbd> to open one. Pressing
<kbd>Enter</kbd> without choosing a suggestion goes to the full results page,
and the same suggestions appear in the search box on the results page. Turn
the setting off and the field becomes a plain search box.

### Customer accounts

The account icon in the header (and the **Account** button in the mobile
menu) is shown when two things are true: customer accounts are turned on in
**Settings > Customer accounts** in Shopify admin, and **Show account link**
is on in the Header section. What shoppers see then depends on **Account
sign-in** in [Theme settings > Customer accounts](theme-settings.md#customer-accounts):

- **Sign in with Shop** (the default). Shopify's own sign-in. Shoppers sign
  in without a password, and once signed in the icon opens Shopify's account
  menu. This is the option to choose if your
  store uses Shopify's current customer accounts.
- **Classic login**. The icon links to the theme's own login page, where
  shoppers sign in with an email and password. Once signed in, the icon opens
  a small menu with **Account**, **Addresses** and **Sign out** (an expanding
  list in the mobile menu), so shoppers can get to their details from any
  page.

To add Shopify's **Sign in with Shop** button to the login and registration
pages themselves, install the **Shop** sales channel, activate Shop Pay in
**Settings > Payments**, then in the theme editor open the login or
registration page and add the **Sign in with Shop** app block. Without those
steps the button simply doesn't appear; nothing is broken.

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
A **Menu** block has a **Split into two columns** option, which lays a long
list of links out in two columns instead of one tall one. It takes effect on
wider screens and is off by default.

| Setting | What it does |
| --- | --- |
| Brand description | Rich text shown under your logo. Falls back to your store's description from **Settings > General** if left blank. |
| Show social links | Shows icons for whichever profiles are filled in under [Theme settings > Social media](theme-settings.md#social-media). |
| Show country/region selector | A dropdown for switching between the countries or regions your store sells to. Only appears when your store has more than one enabled in **Settings > Markets**. |
| Show language selector | A dropdown for switching between storefront languages. Only appears when your store has more than one published language in **Settings > Languages**. |
| Show payment icons | Shows icons for the payment methods enabled in your store. |
| Show policy links | Links to whichever store policies you've published in **Settings > Policies** (refund, privacy, terms, and so on). |

## Back to top button

A small round arrow button appears in the corner of the screen once a
shopper has scrolled a little way down any page, and takes them smoothly back
to the top when pressed. Turn it off with **Show a back to top button** in
[Theme settings > Layout](theme-settings.md#layout).

## Breadcrumbs

Product, collection, blog, article and page templates show a breadcrumb trail
back to the home page automatically (for example, Home > Collection name >
Product name). The home page itself has no breadcrumb, since it's the root.
There's no setting to configure this; it follows the page you're on.

## Sitemap section

For a simple, in-page index of your store separate from breadcrumbs and the
header menu, add the **Sitemap** section to a page. See
[Sections and blocks](sections-and-blocks.md#sitemap) for what it includes.
