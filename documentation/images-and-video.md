# Images and video

## Focal points

Repose honours the focal point you set on an image in Shopify admin (click an
image, then **Edit focal point**), across hero images, product images,
collection images, and most other places a merchant-chosen image appears.
When a section crops an image to fit its shape, especially on narrower
screens where more of the image is cut away, the focal point keeps your
chosen subject in frame instead of an arbitrary centre crop. The hero section
additionally offers manual focal position presets (left, centre, right, top,
bottom, or automatic) for its desktop and mobile images independently, for
cases where you want more control than the image's own focal point gives you.

## Recommended formats and sizes

Shopify serves every image you upload through its CDN, automatically
generating the resized, next-gen formats each visitor's browser needs. You
don't need to pre-resize images before uploading, but a few things affect
quality and load time:

- **Upload at the largest size you reasonably have.** The theme requests
  a range of sizes from the same source image, from small thumbnails up to
  roughly 2400px wide for hero and gallery images, so an undersized source
  image will look soft at larger sizes.
- **JPEG for photography, PNG for anything needing transparency** (logos,
  icons). Shopify converts to modern formats like WebP automatically where a
  visitor's browser supports it.
- **Match your aspect ratio to the setting.** Where a section offers an
  image ratio choice (square, portrait, adapt to image), cropping happens
  automatically, but starting from an image close to that ratio, with the
  subject centred or focal-pointed correctly, gives the cleanest result.
- **Logos**: upload at least 520px wide for a crisp result at the largest
  logo width setting (260px), since the theme requests higher-resolution
  logo images for high-density (retina) screens.
- **Favicons**: a square image at least 64x64px.

## Lifestyle fallback images

If a hero section has no image chosen yet, it falls back to a bundled
placeholder image rather than showing an empty banner. Which one shows is
controlled by the **Lifestyle fallback style** setting under
[Theme settings > Brand](theme-settings.md#brand), with around 20 styles to
choose from, each themed toward a different kind of store (home and
interiors, clothing, jewellery, coffee and home fragrance, and so on). This
is meant as a placeholder while you're setting up, or a graceful fallback if
a hero's image is ever removed, not a substitute for your own photography.
As soon as you choose an image for a hero section, your image always takes
priority over the fallback. Set the style to "None" to show no fallback
image at all.

These fallback images are bundled with the theme itself; they are never
uploaded to your store's Files, so they don't count toward your file storage.

## Video and 3D models

Product pages support Shopify-hosted video (with an optional loop setting in
the gallery), external video embeds, and 3D models, alongside regular
images, all in the same gallery. 3D models show a small badge in the
thumbnail strip so shoppers can tell before opening them. The gallery's zoom
styles (lightbox, external zoom, loupe) apply to images only; video and 3D
model media play or rotate in place instead. See
[Products and collections](products-and-collections.md#gallery) for the
gallery's other settings.

## Social sharing images

Set a **Default social sharing image** under
[Theme settings > Brand](theme-settings.md#brand) for link previews on
social media and messaging apps, used whenever a product, collection,
article or page doesn't have its own share image set individually in
Shopify admin.
