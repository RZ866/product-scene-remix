# Generation rules

## Input roles

- The scene reference defines scene type, camera angle, composition, placement, perspective, depth, lighting, and narrative.
- Product references define product identity and take priority over the original object's shape.

## Complete replacement

Before generation, create a replacement inventory containing:

- target product classes to replace;
- non-target products and objects to preserve;
- every complete, partial, cropped, obscured, distant, and reflected target instance;
- target product imagery on signs, posters, screens, labels, and packaging;
- original accessories or packaging tied to each target.

Replace every target instance in the inventory. Do not replace unrelated non-target products merely because they are visible. When the user explicitly requests replacing all products, treat all product classes as targets unless doing so would conflict with another explicit instruction.

Remove incompatible remnants such as original lids, handles, straws, sticks, smoke, ribbons, labels, logos, decorations, or packaging. Never create hybrid products.

Follow the configured product distribution. In one-output-per-product mode, use exactly one saved product identity throughout each output. In mixed mode, use only supplied products and follow requested quantities and positions.

## Identity and proportions

Preserve silhouette, width-to-height ratio, material, color, transparency, finish, closure, label placement, and distinctive features. Never stretch, compress, recolor, or structurally deform a product to fit the original footprint. Adjust spacing, count, dividers, or density instead.

When a replacement product is materially taller or wider than the original, reduce product count, increase spacing, adjust dividers, or change display density to preserve plausible physical clearance. Never shrink a product below a realistic scene scale merely to retain the original count.

## Composition and realism

Preserve scene category, main camera angle, perspective, important structures, and narrative. Match surface contact, shadows, reflections, ambient color, highlights, depth of field, occlusion, and scale by distance. Avoid floating objects, pasted edges, inconsistent lighting, and exact cloned repetitions.

Preserve the reference orientation and aspect ratio by default. Retain the original pixel dimensions when the host supports them. Otherwise use the closest supported resolution and crop or extend naturally without stretching the image.

## Mandatory scene differentiation

Every generated output must include deliberate secondary-detail differentiation from the scene reference, even when the user requests only one image. Replacing the main product alone is not sufficient.

For every output, adjust at least two suitable non-product secondary categories:

- density, spacing, or subtle rotation;
- trays, risers, dividers, baskets, mats, tissue, cushioning, or cardboard;
- plants, flowers, foliage, vases, or planters;
- towels, fabric, folds, colors, or stack height;
- existing ornaments and supporting props;
- light direction, brightness, temperature, or shadow softness;
- crop, negative space, depth of field, or subtle background tone.

The changes must be visible and intentional rather than accidental generation noise. Preserve the reference's core scene, camera logic, and narrative while giving the result its own supporting-detail treatment.

When producing multiple outputs, each output must differ both from the scene reference and from the other outputs. Do not reuse the same decoration set, prop arrangement, lighting treatment, or secondary-detail plan unchanged across the set.

Keep changes within the original scene's functional language. Do not introduce unrelated objects, people, clutter, text, or a new narrative. Decorations must remain secondary and must not obscure the product.

Do not alter an element the user explicitly requires to remain unchanged. If fewer than two prop categories can be changed safely, use other permitted secondary categories such as lighting, crop, depth of field, display material, spacing, or background tone instead of skipping differentiation or inventing unrelated decorations.

## Text

Inspect signs, notes, posters, shelf cards, packaging, panels, screens, labels, and overlays. Separate product-specific content from scene-generic content.

Replace or remove original product images, original brand logos, product names, product-specific claims, and packaging copy tied to a replaced product. Preserve scene-generic notices, decorative writing, location or store text unrelated to the original product, and text the user explicitly designates for preservation. Do not paraphrase, translate, or invent copy unless requested.

Typography may vary only when requested. Product labels should preserve layout and hierarchy; if prominent generated text becomes gibberish, make a targeted correction. Do not claim pixel-perfect text unless deterministic compositing was used.

When exact text preservation is essential, preserve the original text region if it does not contain the replaced product, or use deterministic text compositing after generation. Inspect required text character by character, including language, line breaks, punctuation, and order. Do not rely solely on generative rendering or claim exact preservation when verification fails.

## Prices

Apply the saved or current price policy. Under `remove`, delete price numbers, decimals used as prices, currency symbols, unit pricing, membership prices, discounts, crossed-out prices, and promotional price badges. Fill the area naturally with matching background, balanced spacing, or approved non-price copy. Never invent a new price.

## Packaging

Apply packaging decisions in this order:

1. Follow the user's current explicit instruction.
2. If the saved product profile includes packaging references, replace product-specific packaging with that verified packaging.
3. If no packaging reference exists, do not invent branded packaging.
4. If the user asks to replace boxes with product units, replace every target box with the corresponding product.
5. Preserve generic shipping cartons as realistic, unbranded, label-free cartons unless the user requests another treatment.

Do not invent plastic bags, sleeves, shrink wrap, cellophane, ribbons, gift boxes, shipping labels, or branded cartons.

## Prompt contract

Every generation request should identify:

- the role of the scene and product inputs;
- every class of object that must be replaced;
- allowed product distribution;
- identity features that must remain faithful;
- scene invariants;
- output-specific secondary variations;
- target and non-target inventories;
- text, price, packaging, aspect-ratio, pixel-size, display-density, and realism policies;
- no original remnants, hybrids, invented brands, unrelated text, watermarks, application UI, unintended packaging, or distorted proportions.
