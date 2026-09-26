# Theme settings

Theme settings apply storewide. Find them in the theme editor under
**Theme settings**, in the left-hand panel. They're organised into the
groups below, in the order they appear in the editor.

## Brand

| Setting | What it does |
| --- | --- |
| Logo | Your store logo, shown in light mode, and in dark mode too if no dark-mode logo is set below. |
| Logo (dark mode) | Optional. Replaces the logo above when a visitor is in dark mode, useful if your main logo doesn't read well on a dark background. |
| Logo width | The logo's display width, from 80 to 260px. |
| Favicon | The browser-tab icon, shown in light mode and in dark mode too if no dark favicon is set. |
| Favicon (dark mode) | Optional dark-mode favicon. |
| Default social sharing image | Used when a product, collection, article or page doesn't have its own image, for link previews on social media and messaging apps. |
| Lifestyle fallback style | A bundled placeholder image style (Nordic, Classic, Elegant or None), used by the hero section when no image has been chosen for it yet. See [Images and video](images-and-video.md#lifestyle-fallback-images). |

## Light colour palette / Dark colour palette

Two matched palettes, one for light mode and one for dark mode, each with the
same ten roles: page background, surface, alternative surface, text, muted
text, borders, primary action (and text on primary), and secondary action
(and text on secondary). Primary action is your main button and link colour;
secondary action is used for less prominent actions and accents.

Keep text-on-colour pairs (text on primary, text on secondary) at accessible
contrast against the colour they sit on, in both palettes. See
[Accessibility](accessibility.md) for the contrast levels the theme is built
to meet.

## Colour mode

| Setting | What it does |
| --- | --- |
| Default mode | Whether new visitors see the light palette, the dark palette, or whichever their device is set to ("Follow device"). |
| Show light and dark mode switcher | Adds a toggle to the header so visitors can switch manually. |
| Remember visitor choice | When on, a visitor's manual choice is remembered on their next visit (stored in their browser only, not tied to their account). |

Repose resolves colour mode before the page paints, so there's no flash of
the wrong palette on load.

## Basket and checkout

| Setting | What it does |
| --- | --- |
| Show accelerated checkout on basket page | Shows Shop Pay and other accelerated checkout buttons on the cart page, alongside the regular checkout button. |
| Show accelerated checkout in drawer and minicart | Same, for the cart drawer and minicart popup. |
| Show free delivery progress bar | Shows a progress bar in the cart working toward a free delivery threshold. |
| Free delivery threshold | The order value, in your store's currency, at which delivery becomes free. Set to 0 to hide the bar entirely. |

Accelerated checkout buttons themselves come from the payment methods you've
enabled in Shopify, and cannot be restyled beyond the unbranded button, per
Shopify's Theme Store requirements. Configure whether the cart icon opens a
drawer, a small popup or the cart page from the **Header** section, covered in
[Navigation and menus](navigation-and-menus.md).

The free delivery bar is a presentational aid only. It does not create a
shipping discount or a free shipping rate: set that up in
**Settings > Shipping and delivery**, matching the same threshold you enter
here.

## Typography

Fonts are chosen from Shopify's font library (system, web-safe and Google
fonts), so there's no file to upload and no performance cost beyond what you
choose to load. Repose uses four font roles:

| Setting | Used for |
| --- | --- |
| Paragraph and body font | Body copy. |
| Display and H1 font | The largest heading on a page. |
| H2 to H6 font | All other headings. |
| Navigation, buttons and labels font | Interface text: menus, buttons, form labels. |

Below the font pickers, a set of sliders controls the type scale: paragraph
size, small text size, navigation and button size, paragraph letter spacing,
space after paragraphs, and body line height for body text; maximum H1, H2
and H3 size, heading line height and heading letter spacing for headings; and
a maximum line length (in characters) for both body text and headings, so
lines of text don't run uncomfortably wide on large screens.

## Layout

| Setting | What it does |
| --- | --- |
| Maximum content width | The page's maximum width on large screens. |
| Maximum section spacing | The largest gap between stacked sections. |
| Maximum page gutter | The largest left/right margin around content. |
| Maximum grid gap | The largest gap between items in a grid. |

Product and collection card grids are adaptive: they add or remove columns
automatically based on the width of the section they're in, rather than a
fixed column count. Minimum and maximum width sliders for product cards and
collection cards control that range, so cards don't become too cramped on
narrow screens or too large on wide ones.

## Buttons and forms

Controls the shape and size of buttons and form fields storewide: button
corner radius, input corner radius, control height, and whether button labels
are shown in uppercase.

## Cards

| Setting | What it does |
| --- | --- |
| Card corner radius | Corner rounding on product and collection cards. |
| Card style | Minimal, outlined or elevated. |
| Product image ratio | Adapt to image, square or portrait, for product card thumbnails. |
| Show vendor on product cards | Shows the product's vendor above its title. |
| Show variant summaries on product cards | Shows a short summary of variant options (such as available colours) on the card. |
| Show quick add for single-variant products | Shows a quick add-to-cart control on cards, for products with only one variant. |
| Show currency codes | Adds the three-letter currency code (for example, USD) next to prices. |

Product cards with more than one image show the second image when a shopper
hovers over the card or moves keyboard focus to it, so a lifestyle or back view is one glance away. Put the
image you want shown on hover second in the product's media list.

## Motion

| Setting | What it does |
| --- | --- |
| Enable subtle reveal animations | A brief entrance animation as content scrolls into view. |
| Enable product-card image zoom | A subtle scale on hover over a product card's image. |

Both respect a visitor's reduced-motion operating system setting
automatically: turning them off here is for merchants who'd simply rather not
have animation, not something needed for accessibility compliance on its own.

## SEO and tracking

Page titles, meta descriptions, and canonical URLs mostly come from Shopify's
own SEO fields on each product, collection, page and article (under
**Edit website SEO** when editing that item). Shopify also generates
hreflang tags, `sitemap.xml` and `robots.txt` automatically; none of that is
configured here.

The theme adds the rest automatically, with nothing to set up: structured
data (schema.org) for your organisation, site search, breadcrumbs, products
with their price, availability and brand, collections and blog articles, so
search engines can show rich results; and Open Graph and X card tags, so
links shared on social media and messaging apps show a title, description
and image.

| Setting | What it does |
| --- | --- |
| Homepage meta description | Shown to search engines for the homepage only. Falls back to your store's own description in **Settings > General** if left blank. |
| Google verification token | The content value from a Google Search Console HTML tag verification, not the full tag. |
| Microsoft Bing verification token | The content value from `msvalidate.01`. |
| Pinterest verification token | The content value from a Pinterest domain claim tag. |
| Meta domain verification token | The content value from a Meta (Facebook) domain verification tag. |
| Google tag ID | An optional storefront page-view tag (for example, a `G-`, `GT-` or `AW-` id). Leave blank if Google Analytics is already installed through the Google & YouTube app, Shopify's Customer Events, or another app, to avoid double-counting. The tag waits for a visitor's analytics consent and is disabled inside the theme editor. For purchase and checkout conversion tracking, use **Settings > Customer events** in Shopify admin instead. |
| Enable custom storefront code | Turns on two free-text code slots below, for a trusted third-party snippet. |
| Code before closing head / Code before closing body | Paste a complete, trusted snippet (including its own `<script>` or `<meta>` tags). These run on the storefront only, never in checkout or the theme editor. For checkout and purchase conversion events, use a Shopify app pixel or custom pixel instead: this slot cannot see checkout. Incorrect code here can affect site performance or break other scripts, so only paste code you trust. |

## Social media

Add your store's profile URLs for Instagram, Facebook, TikTok, Pinterest and
YouTube. These populate the social icons in the footer (when **Show social
links** is on there) and are used for social meta tags where applicable.
Leave any of them blank to omit that icon.
