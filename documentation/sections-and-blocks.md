# Sections and blocks

Every page in Repose is built from sections, added and arranged in the theme
editor. Some sections accept blocks: smaller, repeatable pieces of content
you can add, remove, reorder and sometimes restyle individually. This page
covers every section and block the theme ships, grouped by where you'll use
them. Settings named here are the ones worth knowing about going in; every
section also has its own settings panel in the editor with full descriptions.

For the header, footer and cart, see
[Navigation and menus](navigation-and-menus.md). For the product page and
collection and search pages, see
[Products and collections](products-and-collections.md).

## Homepage and content sections

These are general-purpose sections available on the home page and on pages
using the **Page** template. Add them from the theme editor's **Add section**
button.

### Hero

A large banner, typically the first thing on a homepage. Supports a separate
desktop and mobile image, independent focal-point control for each (or
automatic, which uses the image's own focal point), an eyebrow, heading,
body text, two optional buttons, an image overlay for text legibility, a
translucent content panel option, and controls for horizontal and vertical
content position, text alignment, and desktop and mobile height.

Set **Heading level** to H1 only for the primary hero on your homepage; use
H2 for any other hero elsewhere on the page or site, since a page should
have one H1. If no image is chosen, the hero falls back to a bundled
lifestyle image based on your **Lifestyle fallback style** theme setting; see
[Images and video](images-and-video.md).

### Rich text

Freeform text content in up to four block types: **eyebrow**, **heading**,
**text**, and **buttons** (a primary and secondary button). Add, remove and
reorder these blocks to build simple text-led content. Section settings
control text alignment, maximum content width, and background (page
background, surface, or an alternative surface colour).

### Image with text

A single image paired with an eyebrow, heading, text and a button, with the
image positioned left or right.

### Multicolumn

Up to 6 columns, each an image or icon (choose from a small built-in icon
set, or none), a heading, text and an optional link. Good for feature
callouts, service promises, or a benefits row. Background works the same as
rich text: background, surface, or alternative surface.

### Collection list

A grid of up to 8 collection cards. Each block picks a collection, and can
override its image and title for the card without changing the collection
itself. Grid size (compact, standard or spacious) and an optional "view all"
link are set on the section.

### Featured collection

Pulls products from one collection you choose, showing 2 to 12 of them.
Grid size and a small-screen layout choice (dynamic, one column, or two
columns) control how the grid responds on narrower screens; the grid also
adapts automatically to the width of whatever container it's in. Includes an
optional "view all" link to the full collection.

### Testimonials

Merchant-entered customer quotes, up to 6 per section. Each testimonial block
has an optional photo, a star rating (set to 0 to hide it), a quote, a name
and a role or location. Useful for social proof with no review app
installed, since Shopify has no store-level review feature of its own for a
theme to draw from.

### Trust row

A row of up to 5 short trust signals (free delivery, returns, guarantee,
secure checkout, and so on), each an icon and a line of text. Leave a block's
text blank to hide that item without deleting it.

### Newsletter

An email signup form with an eyebrow, heading and text, connected to
Shopify's built-in customer email marketing signup.

### Contact form

A simple contact form with an eyebrow, heading, body text and Shopify's
built-in contact form. An optional phone field can be added, and the heading
can be centred.

### Collapsible content blocks (flexible blocks)

A general-purpose container section that accepts theme blocks and app
blocks, useful for building an FAQ, a spec sheet, or any layout not covered
by a dedicated section. Content width can be set to narrow, standard or full.
The theme blocks available here include:

- **Metafield accordion**: a collapsible accordion built from product
  metafields or static content, covered in
  [Products and collections](products-and-collections.md#specification-accordions).
- **Map**: an embedded Google Map with an address and directions link,
  covered below.
- **Share**: social share links, covered below.
- Any app block from an installed app.

### Map (theme block)

Embeds a Google Maps location from a share/embed URL, with an address or
location text, an optional directions link, a heading (or none), and control
over whether the map loads immediately or only once a visitor clicks to load
it (better for performance, since embedded maps are heavy). Height and
corner radius are adjustable.

### Share (theme block)

Social share links for the current page: native device share (on supporting
browsers), Facebook, X, Pinterest, LinkedIn, WhatsApp, email and copy link,
each individually toggleable. Display as icons only or icons with labels.

### Custom Liquid

Drops in your own Liquid code or embed snippets, with an option to run full
width. Available both as a section and, on the product page, as a block. Use
sparingly: unlike every other section, the theme cannot guarantee its
accessibility or performance, and no other documentation page covers what
custom code does.

### Apps

A dedicated slot for app blocks (`@app`), with an option to allow app content
to run full width. Add this section anywhere you want an app's embedded
content to appear, then add the app's own block inside it from the block
list.

### Theme demo grid

A gallery-style section that links out to other example storefronts, useful
if you'd like to show visitors (or yourself, while deciding) what the
theme's other presets look like. Each **style** block is a heading,
description, image and a link, either to another unpublished theme via its
preview theme ID or to any custom URL. Most stores won't need this section;
it exists for cases like a marketing or landing page that compares looks.

## Utility and legal sections

### Sitemap

A simple, text-based index of your store's pages, collections, blogs and
policies, with a customisable heading for each column. Useful as a fallback
navigation aid, separate from Shopify's own `sitemap.xml` used by search
engines.

### Announcement bar

Up to 3 rotating messages at the very top of the site, each with optional
text and a link. An option adds separators between messages.

### Blog and article

The **Blog** section controls articles per page, desktop column count (3 or
4), and whether the author and an excerpt are shown on the blog listing. The
**Article** section controls whether the author is shown on an individual
post. Both use Shopify's built-in blog and article content; there's no
separate blocks system here.

### 404, password, and customer account pages

The **404** section has no settings; customise the page itself through your
store's general "page not found" content in Shopify admin. The **Password
page** section (shown while your store is password protected, before
launch) has a single setting to show or hide your logo, and otherwise
inherits the storewide colour palette automatically. The customer account
sections (login, register, account, addresses, order, activate account,
reset password) render Shopify's standard customer account flows styled to
match the rest of the theme, and have no settings of their own beyond what
Shopify's own customer account configuration provides in
**Settings > Customer accounts**.

## Gift cards

The gift card template renders the Shopify-issued gift card page (the one a
customer reaches from their order confirmation or gift card email), styled
to match the theme, including the balance, redemption code and a printable
version. There is nothing to configure here beyond the storewide theme
settings.
