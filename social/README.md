# Social preview images

Consistent 1280×640 social-preview cards for the flagship repositories. These images are designed for link previews on GitHub and other services.

GitHub social previews are repository settings, separate from the image files committed here. Verify them in each repository under **Settings → General → Social preview**. Upload the 1280 × 640 PNG there when it is not already active:

> Repo → **Settings** → **General** → **Social preview** → **Edit** → upload the `.png`.

| Repo | File |
|---|---|
| [repopact-core](https://github.com/ForgeWireLabs/repopact-core/settings) | `repopact-core.png` (source SVG: `repopact-core.svg`; authoritative product asset lives in Core) |
| [repopact-workbench](https://github.com/ForgeWireLabs/repopact-workbench/settings) | `repopact-workbench.png` (source SVG: `repopact-workbench.svg`; authoritative product asset lives in Workbench) |
| [skillforge-academy](https://github.com/JeremyShows/skillforge-academy/settings) | `skillforge-academy.png` |
| [ForgeWire-Overview](https://github.com/ForgeWireLabs/ForgeWire-Overview/settings) | `ForgeWire-Overview.png` |
| [ForgeWireLabs (org profile)](https://github.com/ForgeWireLabs/ForgeWireLabs/settings) | `ForgeWireLabs.png` |
| ForgeWire Labs portfolio | `asset-inventory.json` lists the profile hero and all social-card SVG/PNG pairs |

The `.svg` source files are kept alongside each generated `.png`. Core and Workbench also maintain product-specific cards in their own repositories. Regenerate from the matching SVG and verify the dimensions and hash listed in `asset-inventory.json` before upload.
