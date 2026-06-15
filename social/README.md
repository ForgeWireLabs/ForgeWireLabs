# Social preview images

Consistent 1280×640 social-preview cards for the flagship repositories. These set
the image people see when a repo link is shared on X, LinkedIn, Slack, Discord, etc.

GitHub has **no API** for social previews — each must be uploaded by hand:

> Repo → **Settings** → **General** → **Social preview** → **Edit** → upload the `.png`.

| Repo | File |
|---|---|
| [forgewire-fabric](https://github.com/ForgeWireLabs/forgewire-fabric/settings) | `forgewire-fabric.png` |
| [repopact](https://github.com/ForgeWireLabs/repopact/settings) | `repopact.png` |
| [skillforge-academy](https://github.com/ForgeWireLabs/skillforge-academy/settings) | `skillforge-academy.png` |
| [ForgeWire-Overview](https://github.com/ForgeWireLabs/ForgeWire-Overview/settings) | `ForgeWire-Overview.png` |

The `.svg` source files are kept alongside each `.png`. To re-render after an edit:

```bash
rsvg-convert -w 1280 -h 640 forgewire-fabric.svg -o forgewire-fabric.png
```
