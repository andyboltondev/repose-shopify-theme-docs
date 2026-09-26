# Products and collections

## The product page

The main product section (**Product information**) is built entirely from
blocks, so you can add, remove and reorder almost everything on the page:
vendor, title, rating, trust row, price, variant picker, quantity selector,
buy buttons, description, collapsible rows (accordions), share links, a map,
custom Liquid, and app blocks. Add, remove and reorder them from the theme
editor to change the page's structure without touching code.

A few blocks have settings worth knowing about:

- **Buy buttons**: **Show dynamic checkout button** adds Shop Pay, Apple Pay
  or another accelerated checkout button under add to cart, depending on the
  payment methods you have enabled.
- **Collapsible row**: a heading with either rich text or the content of a
  page you choose, so shared text such as a delivery policy is written once
  and reused on every product.
- **Trust row**: up to four short reassurances (delivery, returns, guarantee,
  secure checkout), each an icon and a line of text. Leave an item's text
  blank to hide it.
- **Variant picker**: shows each option's values as buttons. When the
  chosen combination is sold out or doesn't exist, the add to cart button
  says so instead of adding it.

### Gallery

The product image gallery has its own settings, separate from the blocks
above:

| Setting | What it does |
| --- | --- |
| Gallery media ratio | Adapt to the featured image, square, or portrait. |
| Gallery media fit | Fit the entire media in frame, or fill the frame (cropping). |
| Show gallery thumbnails | Toggles a thumbnail strip. |
| Desktop thumbnail position | Below the main media, or beside it on the left. |
| Show previous and next buttons | Arrow controls on the main image. |
| Loop Shopify-hosted videos | Whether uploaded product videos loop automatically. |
| Image zoom style | How a shopper gets a closer look. See below. |

**Image zoom style** has four options:

- **None**: no zoom interaction.
- **Lightbox**: clicking an image opens a larger, fullscreen view.
- **External zoom**: hovering shows a magnified view in a panel beside the
  gallery.
- **Loupe**: hovering shows a small magnifying lens that follows the cursor,
  with an adjustable lens size. Best on narrower desktop windows, where an
  external panel wouldn't fit.

All three interactive styles include a touch path (tap to open the lightbox,
with pinch-to-zoom and swipe) and a keyboard path (open with Enter, pan with
arrow keys, close with Escape). Video and 3D model media aren't affected by
the zoom style; they play or rotate in place instead.

### Keeping details visible while scrolling

**Keep product details visible while scrolling** (desktop only) keeps the
title, price and buy buttons in view beside a tall gallery, instead of
scrolling past them.

**Show a sticky add to cart bar while scrolling** shows a slim add-to-cart
bar once the buy buttons block scrolls out of view, so the buy button is
always reachable. This requires a buy buttons block to be present in the
section; without one, there's nothing for it to track.

### Colour swatches

Options such as colour, metal or finish can show as swatches instead of text
buttons. An option shows as swatches when its name is in **Theme settings >
Swatches > Swatch option names**, or when Shopify already has swatch data for
it.

Each swatch takes its look from, in order:

1. **The swatch set in Shopify admin.** If the option is linked to a colour
   metafield (the category metafield Shopify offers for colour options), the
   colour or pattern image you chose there is used.
2. **The variant's image.** Otherwise the swatch shows the image of the
   variant that value selects, so a product whose variants already have
   images gets swatches with no extra setup. Assign each variant's image
   under **Products > select product > the variant > image**.

A value with neither shows as a text button, so nothing ever disappears.
Swatches show no text of their own, so the option's label names the selected
value (for example, "Colour: Charcoal"), and screen readers hear the value
name.

Filters show swatches when you set a filter's display to swatches in Shopify's
Search & Discovery app, which requires the option to be linked to a colour
metafield.

### Variant image grouping

You can control which images appear for which variant by adding rules to an
image's **alt text** in Shopify admin, under
**Products > select product > click the media item > Add alt text**. Always
write the real, accessible description of the image first; the matching
rules are added after it.

Rules start with a single `#` and use the product's own option names and
values, in quotes:

| You want | Write |
| --- | --- |
| Match one option value | `#"Colour" is "Blue"` |
| Exclude a value | `#"Logo" is not "Yes"` |
| Match either of two values | `#"Case Style" is "Rugged" or "Case Style" is "Armoured"` |
| Match any of several options | `#"Primary Colour" is "Red" or "Secondary Colour" is "Red" or "Tertiary Colour" is "Red"` |
| Match a combination | `#"Colour" is "Blue" and "Finish" is "Gloss"` |
| Group combinations | `#("Item 1" is "Red" and "Size 1" is "Small") or ("Item 2" is "Red" and "Size 2" is "Small")` |

A complete alt text field looks like:

```
front view of blue phone case #"Colour" is "Blue"
```

Rules: use exactly one `#` at the start of the rules block. Put option names
and values in quotes. Matching is case-insensitive. Supported keywords are
`is`, `not`, `and`, `or`. Use parentheses to combine `and` and `or` groups.
Any image with no rules is shared by all variants and always shows.

How the gallery treats your rules:

- **Only the description reaches shoppers.** Everything before the `#` is
  used as the image's alt text wherever the theme shows it: the product
  gallery, product cards, the cart, search results and social sharing
  previews. Screen readers never hear the rules. If there is no description
  before the `#`, the product title is used instead.
- **Don't use `#` in the description itself.** A `#` with a space before it
  starts the rules block, so `size #2 mixing bowl` is read as a broken rule.
  Write `size 2 mixing bowl` instead.
- **`and` is checked before `or`.** `"Colour" is "Blue" or "Finish" is "Gloss"
  and "Size" is "Large"` means blue, or glossy and large. Use parentheses when
  you mean something else.
- **Curly quotes work.** Quotes typed on a phone or pasted from a word
  processor (`“Colour”`) are treated the same as straight ones.
- **A rule with a mistake hides its image.** An unclosed quote, a missing
  `is` or an unclosed parenthesis makes the rule invalid, and that image stays
  hidden for every variant. Your browser's developer console shows a warning
  naming the rule.
- **The gallery never goes blank.** If a mistake means no image matches the
  selected variant, the gallery shows every image rather than none, so
  shoppers are never left without a picture.

### Ratings

The **Rating** block reads the standard `reviews.rating` and
`reviews.rating_count` metafields, the fields every major Shopify review app
writes to, and renders nothing if either is missing. If you haven't
installed a review app yet, remove or ignore this block until you have;
Shopify's own free Product Reviews app has been discontinued, so ratings
require a third-party review app. The same metafields also drive the star
rating shown on product cards throughout the store.

### Specification accordions

The **Metafield accordion** theme block, added inside a **Flexible blocks**
section (the default product template has one below the product
information), builds an accordion from metafields, useful for
specifications, care instructions or sizing details without retyping them
into a rich text block for every product. It is built in three levels:

- **Metafield accordion**: the container. It holds the styling: an optional
  header, whether one or several items can be open at once, vertical or
  horizontal layout on larger screens, chevron or plus and minus icons,
  sizes, padding, borders, and either the theme's colours or your own.
- **Accordion item**: one collapsible panel, with a title and an option to
  open it by default. Its **Display type** is either **Content**, one block
  of rich text, or **Table**, a two-column list of labels and values built
  from rows.
- **Metafield row**: one label and value in a table item.

Content and row values can each come from a **Dynamic source** (connect a
metafield with the editor's dynamic source button, or type static text), or,
for metafield types that can't be connected that way, from a **Metafield
namespace and key** you type in. For a metafield that references a
metaobject, enter the metaobject field to display (such as `name` or
`title`) under **Metaobject display field**.

Empty content hides automatically, so one accordion works across products
with different metafields: a row with no value is hidden unless you turn on
**Show blank table values**, and an item with nothing to show is hidden
entirely.

### Pre-order and back-order labelling

Repose labels stock automatically. Product cards show **Sold out** when
nothing can be bought, **Sale** when a compare-at price is higher than the
price, and **Back order** when a product is set to **Continue selling when
out of stock** and has reached zero. The product page shows the same for the
selected variant (**Out of stock** or **Back order**), updating as the
shopper changes options. Add the tag `pre-order`, `pre order` or `preorder`
to a product to have oversold stock labelled **Pre-order** rather than back
order, in both places.

### Product recommendations

A separate section, typically placed below the main product section, with
a heading, the number of products to show and a grid size. Choose
**Related products** (Shopify's automatic "customers also viewed"-style
matching) or **Complementary products**, which uses pairings you curate
per-product in Shopify's free Search & Discovery app. Complementary
recommendations only appear once you've set up pairings there; until then,
the section shows nothing for that product.

The cart drawer, minicart and cart page also suggest up to four
complementary products for the first item in the cart, from the same
Search & Discovery pairings. With no pairings, nothing is shown.

## Alternate templates

Some page types have more than one template available, giving you a
different section layout for specific products, collections or pages
without affecting the rest of your catalogue:

- **Product**: the default template, or an **Editorial** template with a
  leaner set of purchasing blocks, suited to a photography-led product page.
  Both use the same product section and gallery settings described above;
  what's actually turned on for each is something you set, and can change,
  in the theme editor.
- **Collection**: the default template, or an **Editorial** template that
  adds an image-with-text story section above the product grid.
- **Page**: ready-made **About**, **Landing** (hero, featured collection,
  story, testimonials, newsletter), **FAQ** (a flexible blocks section with
  a metafield accordion for questions and answers) and **Sitemap**
  templates, alongside the default page template. The contact page uses the
  **Contact form** section; see
  [Sections and blocks](sections-and-blocks.md#contact-form).

To use one, open the product, collection or page in Shopify admin, and in
the **Theme template** panel on the right, choose the alternate template
from the dropdown. This doesn't move or duplicate the item; it only changes
which section layout renders it.

## Collection pages

The **Collection products** section controls:

| Setting | What it does |
| --- | --- |
| Show description | Shows the collection's description above the grid. |
| Show collection image | Shows the collection's banner image. |
| Enable filtering | Turns on the filter panel (facets), built from your store's product options, tags, availability, price, and other filterable properties, powered by Shopify's native filtering. |
| Enable sorting | Turns on the sort dropdown. |
| Products per page | How many products load per page. |
| Product size | Compact, standard or spacious grid density. The grid also adapts automatically to the width of the product area, including when filters are visible. |
| Small-screen layout | Dynamic, one column, or two columns, for narrow viewports. |

The **Collection list page** section (the page listing all your
collections) has similar grid density controls, plus a heading and a colour
setting for card text, which sits over a dark gradient at the base of each
card image so it stays legible over any photo.

## Search results

The **Search results** section offers the same filtering and sorting toggles
as collection pages, plus a results-per-page setting. Filtering, sorting and
search itself are all powered by Shopify's native search and filtering, no
app required for the baseline experience.
