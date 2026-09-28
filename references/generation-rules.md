# Generation rules

## Input roles

- The scene reference defines scene type, camera angle, composition, placement, perspective, depth, lighting, and narrative.
- Product references define product identity and take priority over the original object's shape.

## Complete replacement

Replace every requested original product, including complete, partial, cropped, obscured, distant, reflected, transparent-container, printed, poster, screen, and packaging instances when applicable.

Remove incompatible remnants such as original lids, handles, straws, sticks, smoke, ribbons, labels, logos, decorations, or packaging. Never create hybrid products.

Follow the configured product distribution. In one-output-per-product mode, use exactly one saved product identity throughout each output. In mixed mode, use only supplied products and follow requested quantities and positions.

## Identity and proportions

Preserve silhouette, width-to-height ratio, material, color, transparency, finish, closure, label placement, and distinctive features. Never stretch, compress, recolor, or structurally deform a product to fit the original footprint. Adjust spacing, count, dividers, or density instead.

## Composition and realism

Preserve scene category, main camera angle, perspective, important structures, and narrative. Match surface contact, shadows, reflections, ambient color, highlights, depth of field, occlusion, and scale by distance. Avoid floating objects, pasted edges, inconsistent lighting, and exact cloned repetitions.

## Differentiated variants

For multiple outputs, vary at least two secondary categories when appropriate:

- density, spacing, or subtle rotation;
- trays, risers, dividers, baskets, mats, tissue, cushioning, or cardboard;
- plants, flowers, foliage, vases, or planters;
- towels, fabric, folds, colors, or stack height;
- existing ornaments and supporting props;
- light direction, brightness, temperature, or shadow softness;
- crop, negative space, depth of field, or subtle background tone.

Keep changes within the original scene's functional language. Do not introduce unrelated objects, people, clutter, text, or a new narrative. Decorations must remain secondary and must not obscure the product.

## Text

Inspect signs, notes, posters, shelf cards, packaging, panels, screens, labels, and overlays. Preserve meaningful scene text by default: wording, language, important line breaks, approximate placement, and hierarchy. Do not paraphrase, translate, or invent copy unless requested.

Typography may vary only when requested. Product labels should preserve layout and hierarchy; if prominent generated text becomes gibberish, make a targeted correction. Do not claim pixel-perfect text unless deterministic compositing was used.

## Prices

Apply the saved or current price policy. Under `remove`, delete price numbers, decimals used as prices, currency symbols, unit pricing, membership prices, discounts, crossed-out prices, and promotional price badges. Fill the area naturally with matching background, balanced spacing, or approved non-price copy. Never invent a new price.

## Packaging

Do not invent plastic bags, sleeves, shrink wrap, cellophane, ribbons, gift boxes, shipping labels, or branded cartons. Preserve generic scene packaging unless asked to change it. Replace product-specific packaging when required by the current request or supplied references.

## Prompt contract

Every generation request should identify:

- the role of the scene and product inputs;
- every class of object that must be replaced;
- allowed product distribution;
- identity features that must remain faithful;
- scene invariants;
- output-specific secondary variations;
- text, price, packaging, aspect-ratio, and realism policies;
- no original remnants, hybrids, invented brands, unrelated text, watermarks, application UI, unintended packaging, or distorted proportions.

