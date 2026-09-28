---
name: product-scene-remix
description: Create ecommerce product-scene images by replacing every original product in a reference scene with products from the user's persistent product profile. Use when the user says “开始使用”, asks to initialize products, uploads a scene for product replacement, or requests product-scene image remixes.
metadata:
  display_name: 产品场景二创
  display_name_en: Product Scene Remix
  version: 1.0.0
  author: RZ866
---

# Product Scene Remix

Create product-scene images from a scene reference and the user's own product references. The scene image defines composition and environment. The saved product references define product identity.

Explicit instructions in the current request override defaults in this skill.

## Route by profile state

Before every matching task, check for a valid persistent profile. Read [references/onboarding.md](references/onboarding.md) when the profile is missing, incomplete, unreadable, or explicitly being changed.

Initialization may be triggered by any of these:

- “开始使用”, “初始化产品”, or “建立我的产品档案”;
- an explicit request to configure, reset, or invoke this skill;
- a request such as “替换成我的产品”, “给我的产品做场景图”, or “帮我做商品二创图”;
- a scene reference supplied before a valid profile exists.

If initialization interrupts an existing scene request, retain that scene and request, finish onboarding, and resume automatically. Do not require the user to upload the same scene again.

When the profile is valid, never repeat onboarding. If the user says “开始使用”, ask only for a scene reference.

## Required workflow

1. Load the product profile and its reference images.
2. Treat the current image as the scene and composition reference.
3. Analyze every target instance: foreground, background, cropped, obscured, reflected, printed, screened, or packaged.
4. Decide the output set from the saved defaults and current request.
5. Read [references/generation-rules.md](references/generation-rules.md), then generate or edit each output separately with the host's best suitable image-editing capability.
6. Read [references/quality-checklist.md](references/quality-checklist.md) and inspect every result.
7. Make one targeted correction for visible product-identity, replacement, text, price, packaging, or realism errors; inspect again.
8. Save accepted finals to the configured output directory. Never leave the only final in a temporary generation directory.
9. Return clickable paths or links for every final.

## Image tool and model

Use the host platform's built-in raster image generation or editing capability. Prefer precise editing/compositing, high reference fidelity, and the highest-quality available setting unless the user prioritizes speed or cost.

When OpenAI image model selection is exposed, prefer `gpt-image-2.5-sunburst` for precision and `gpt-image-2.5-flare` for speed. When the host manages selection internally, use its built-in tool and do not claim a specific underlying model.

Do not silently switch to an external paid API, request an API key, or upload product assets to another service without the user's explicit agreement.

If the host lacks image input, image editing, or persistent file access, explain the unavailable capability. Offer session-only operation when persistence alone is unavailable.

## Output and overwrite

Use the saved output directory unless the current request specifies another location. Use a reference basename, timestamp, and product or variation ID in filenames. Add `-v2`, `-v3`, and so on when a target exists. Overwrite only when explicitly requested.

## Profile maintenance

Update the existing profile when the user adds, removes, replaces, or renames individual products. Reinitialize only when explicitly requested, when the entire library is being replaced, or when the saved profile cannot be recovered.

