# Preview images

`cover.jpg` is included and registered in the manifest. It was composed from an Orca screenshot
using the built-in image generation tool for cleanup and layout, then encoded as JPEG for the
directory's size limit. It is 1586×992 pixels and approximately 164 KiB.

Processing instructions: retain the public theme name, palette and Markdown content; remove
the projects sidebar, local path, work tabs, chat panels and bottom status bar; arrange the
remaining content as a landscape cover on deep teal with the title and subtitle.

The private source screenshot is not included in this repository. The edited cover is an
AI-assisted presentation, not a pixel-exact app capture. Separate editor and terminal
screenshots have not been captured yet. Register their fields only after the files exist.

## Prepare the scene

1. Select **xclas721-theme** for both the dark app theme and the terminal palette.
2. Open `PREVIEW.md` in Orca. Use preview view for the cover, or source view to show Markdown
   syntax colors. A source/preview split can show both. Preview code blocks may use a
   different highlighter from the source editor.
3. Keep the title, palette and code visible. Adjust the editor font size if needed.
4. Include some Orca chrome to show the teal background and mint selection.
5. If a terminal is visible, use this repository and harmless output such as
   `git status --short --branch`. Check for private names, paths, chats or credentials before saving.

## Files to capture

| File | Content | Dimensions | Maximum size |
| --- | --- | --- | --- |
| `cover.jpg` | Included: composed cover based on `PREVIEW.md` in Orca | 1586×992; recommended capture 1600×1000 | 1024 KB |
| `editor.png` | Source editor showing syntax colors | At least 1280×800 | 1536 KB |
| `terminal.png` | Terminal with the matching palette | At least 1280×800 | 1536 KB |

Use a 16:10 cover crop. PNG, JPEG and WEBP are supported; use static images. Save the images in
this directory. Up to six screenshots are supported, with a combined image limit of 8 MB.

An optional square `icon.png` can also be added: PNG or WEBP, at least 128×128, up to 256 KB.
It is separate from the cover and not required for listing.

## Register the images

The cover field is already registered. Once the two additional screenshots exist, extend the
manifest with `screenshots` as below:

```json
{
  "cover": {
    "path": "images/cover.jpg",
    "alt": "AI-composed cover based on xclas721-theme in Orca, showing the Markdown preview and palette with private workspace information removed"
  },
  "screenshots": [
    {
      "path": "images/editor.png",
      "alt": "The Orca editor showing source code with xclas721-theme syntax colors",
      "caption": "Editor syntax colors"
    },
    {
      "path": "images/terminal.png",
      "alt": "The Orca terminal with the xclas721-theme dark teal ANSI palette",
      "caption": "Matching terminal palette"
    }
  ]
}
```

Describe what the actual screenshots show in their alt text. If only the cover is ready, add
only `cover`; leave `screenshots` out until those files exist.

The cover is already displayed below the introduction in the root README.
If an icon is captured, add `"icon": "images/icon.png"` to the manifest too.

Run `orca plugin validate .` after registering the images. Before publishing, bump the plugin
version, update `CHANGELOG.md`, commit, validate again and push a matching new version tag.
Existing tags must continue to point at their original files.

## References

- [Official manifest and image constraints](https://github.com/stablyai/orca/blob/main/docs/reference/plugin-manifest.md)
- [Official publishing guide](https://www.onorca.dev/plugins/add)
