# Quality checklist

Accept an output only after checking the following.

## Product identity

- Correct silhouette and width-to-height ratio
- Correct body color, material, transparency, and finish
- Correct lid, cap, cork, pump, handle, or accessory
- Correct count and structure of reeds, wicks, straps, handles, attachments, and supplied accessories
- Correct label position and visual hierarchy
- Correct label proportions, color blocks, logo area, brand identity, and verified wording
- No mixed, invented, stretched, or compressed product features
- No added, removed, simplified, embellished, recolored, restyled, or redesigned product features
- Product appearance remains consistent across every output unless the user explicitly requested product variants

## Replacement completeness

- A target/non-target replacement inventory was created before generation
- No original foreground product
- No original background or edge product
- No original partial or obscured product
- No original reflected product
- No incompatible original accessories
- No original product image on a sign, screen, or package when replacement is required
- Unrelated non-target products and objects remain unchanged unless explicitly requested

## Physical realism

- Scale matches scene depth
- Perspective is consistent
- Products contact supporting surfaces
- Shadows and reflections are plausible
- Transparent and reflective materials behave naturally
- Repeated products do not look like exact cloned stamps
- Product count, spacing, and display clearance remain plausible for the replacement product's real proportions
- Output orientation and aspect ratio match policy, with no stretched final image

## Text and commercial information

- Preserved text remains semantically unchanged
- Exact required text was checked character by character or composited deterministically
- Original product branding and product-specific claims were removed or replaced as required
- Scene-generic and user-protected text remains intact
- Requested replacement text is correct
- No prominent gibberish
- Price handling follows policy
- No watermark, UI badge, or unintended overlay

## Differentiation

- Every output, including a single-image request, has visible secondary-detail differentiation from the scene reference
- Product replacement itself is not counted as differentiation
- The protected target product was not used as a differentiation variable
- At least two suitable non-product secondary categories were deliberately adjusted unless the user explicitly protected those elements
- With multiple outputs, every output differs from both the reference and the other outputs
- Decoration sets, prop arrangements, and lighting treatments are not copied unchanged
- Variation does not alter product identity
- Product count or placement changed only when physically necessary or explicitly requested, and the change was minimal
- Supporting props do not obscure or compete with the product

## Packaging

- Packaging follows the current request first
- Verified product packaging is used only when references exist
- No invented branded packaging
- Generic shipping cartons are realistic, unbranded, and label-free when preserved

## Acceptance and retry limit

- Inspect after every generation and correction attempt
- Allow no more than two targeted correction attempts per failed output
- Never mark an output accepted while a required invariant still fails
- Keep successful outputs when another output fails
- Report unresolved failures instead of silently changing model, tool, or external service
