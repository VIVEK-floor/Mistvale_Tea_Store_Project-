# Mistvale Tea Co. — delivery notes

## 1. What I changed
- Replaced the placeholder product imagery with eight consistent, square, web-optimised product images matching the actual PRODUCTS data.
- Added a clean Mistvale wordmark SVG for the header.
- Replaced the hero placeholder with a natural-light tea-garden image and kept the hero copy in HTML rather than baked into the image.
- Converted product images and hero imagery to WebP and resized them for web delivery.
- Kept all product IDs, names, prices, stock and the API object unchanged.
- Kept the checkout form contract and approved footer legal text unchanged.
- Preserved the existing search, category, sort, cart, coupon, delivery, newsletter, FAQ and structured-data functionality.
- Updated image references to use the final WebP assets directly.

## 2. What the AI got wrong
- Early generated product concepts used generic product names that did not match the assessment's PRODUCTS data. I discarded those concepts and mapped the final images to the exact eight products in the kit.
- An earlier working copy referenced missing `.webp` files, which produced `ERR_FILE_NOT_FOUND` in the browser console. I reproduced the problem in Chrome, checked the requested paths, and corrected the asset set and references.
- The checkout URL is intentionally a non-existent `mistvale.example` endpoint. The kit explicitly defines this as expected behaviour, so it was not replaced.

## 3. Images
- Images were created with an AI image-generation tool.
- Product images were cropped to a consistent 1:1 square format and converted to WebP.
- The hero visual was cropped from the generated banner direction to remove baked-in copy so the website renders the heading and CTA as accessible HTML.
- The logo is delivered as SVG.

## 4. How I tested it
- Tested the store in Chrome from the local `index.html`.
- Checked search, category filters, cart quantity controls, remove, sold-out behaviour, coupon threshold behaviour, shipping threshold, checkout submission, newsletter validation and mobile layout.
- Checked the browser Console and fixed the broken image-resource errors.
- Verified final product assets are present and each is under the 150 KB product-image target; the hero is under the 250 KB target.

## 5. Questions for the team
- None at this stage.

## 6. Time spent
- Approximately 4 hours including functional testing, asset preparation and design work.

## 7. Extra features
- Existing quick view and wishlist interactions were retained.
- FAQ accordion and FAQ structured data were retained.

## 8. With more time I would…
- Run a full Lighthouse accessibility/performance pass and refine any remaining keyboard focus-trap details in the drawer/modal.
