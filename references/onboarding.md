# One-time onboarding

Use this workflow only when no valid profile exists or the user explicitly requests configuration changes.

## 1. Collect product references

Ask the user to upload one clear white-background image for each product. Recommend:

- one complete product per image;
- front-facing or primary selling angle;
- accurate color and clear edges;
- no hand, prop, strong shadow, or perspective distortion;
- readable label structure;
- additional side, back, top, closure, or packaging views only when they materially affect accurate reproduction.

Accept a clean transparent-background cutout when it preserves the complete product. Do not invent a missing product or substitute another reference.

## 2. Build the identity profile

For every product record:

- ID and user-facing name;
- category and silhouette;
- width-to-height ratio;
- body material, color, transparency, and finish;
- closure, lid, cap, cork, pump, handle, or accessory;
- label position, proportions, color blocks, logo area, and text hierarchy;
- packaging relationship;
- distinctive features that must not change;
- paths to the persistent reference copies.

Copy references from temporary upload locations into a persistent product library. Never store user products inside the installed skill directory or public repository.

Prefer a host-approved user data directory. A conventional local layout is:

```text
~/.product-scene-remix/
├── profile.json
└── products/
```

If that location is not writable, use `.product-scene-remix/` in the current workspace after informing the user. Never claim cross-device persistence for local files.

## 3. Ask once for the output directory

Ask:

> 请设置生成图片的默认保存位置。以后只需上传参考场景图，结果会自动保存到这里。如果不指定，将使用当前项目中的 `outputs/product-scene-remix/`。

Validate or create the selected directory when permitted. If the user does not choose one, use `outputs/product-scene-remix/`.

## 4. Save defaults

Save JSON with at least:

```json
{
  "profile_version": 1,
  "initialized": true,
  "products": [],
  "output": {
    "directory": "outputs/product-scene-remix",
    "format": "png",
    "overwrite": false
  },
  "generation": {
    "mode": "one-output-per-product",
    "aspect_ratio": "preserve-scene",
    "text_policy": "preserve",
    "price_policy": "remove",
    "packaging_policy": "reference-and-current-request",
    "vary_secondary_decorations": true,
    "minimum_varied_prop_categories": 2
  }
}
```

The user's current choices override these defaults. Do not store secrets, API keys, temporary paths, or unrelated personal information.

## 5. Finish

Tell the user:

> 初始化已经完成。以后只需上传一张参考场景图，我会自动读取产品档案、完成替换并保存到默认目录。

If a scene request was waiting, resume it immediately.

