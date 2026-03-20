# Mod Manager — Mod Repository

This repository hosts the community mod list for the [Mod Manager](https://github.com/Jellyfin-PG/Mod-Manager) Jellyfin plugin. The `mods.json` file is fetched live by the plugin, so approved mods appear in the store without requiring a plugin update.

---

## Submitting a Mod

Mods are added through GitHub issues. Open a new issue and select the **Mod Submission** template. Fill in all required fields and a maintainer will review it.

**Before submitting, make sure your mod meets these requirements:**

- The JS or CSS file is hosted at a stable, publicly accessible URL (GitHub raw or jsDelivr CDN are preferred)
- The mod works without any additional dependencies or local files
- It has been tested on Jellyfin 10.10 or 10.11
- The source is publicly available (GitHub repository or equivalent)

Mods that are abandoned, broken, or require files beyond a single JS or CSS file will not be accepted.

---

## Mod Format

Each entry in `mods.json` uses the following structure:

```json
{
  "id": "my-mod",
  "name": "My Mod",
  "author": "AuthorHandle",
  "description": "One or two sentences describing what the mod does.",
  "version": "1.0.0",
  "type": "js",
  "jellyfin": "10.11+",
  "tags": ["player", "ui"],
  "previewUrl": "https://example.com/preview.png",
  "sourceUrl": "https://github.com/author/my-mod",
  "jsUrl": "https://raw.githubusercontent.com/author/my-mod/main/mod.js",
  "jsInline": null,
  "cssUrl": null,
  "cssInline": null
}
```

The `type` field accepts `"js"`, `"css"`, or `"both"`. For `"both"`, populate the relevant URL or inline fields for each type.

**Available tags:** `ui` `player` `video` `home` `cards` `minimal` `artwork` `badges` `animations` `css` `developer`

---

## License

The contents of this repository are licensed under [MIT](LICENSE). Individual mods remain the property of their respective authors under their own licenses.
