# CabinetOS marketplace index

The public index of the [CabinetOS](https://github.com/OliverD25/cabinetos)
marketplace, served by GitHub Pages at

    https://oliverd25.github.io/cabinetos-marketplace/index.json

CabinetOS reads it when the marketplace view opens, over HTTPS with ETag
caching, and checks every download against the SHA-256 in the index.

## What is here

| Path | Contents |
|---|---|
| `index.json` | The index, schema version 1: one item per extension with its download link, size and SHA-256. |
| `files/` | The extensions themselves. Today: 41 colour themes, one JSON file each. Five ship inside CabinetOS and are listed so the app can show their versions; 36 are the theme collection, ports of well-known editor themes. |
| `NOTICES.md` | The source, author, license and exact commit of every theme in the collection. |
| `LICENSE` | MIT, for the index and the ports. Each theme's colours keep their own license, named in `NOTICES.md`. |

## How it is built

Nothing here is edited by hand. The CabinetOS repository builds this folder
with `sdk/marketplace/build-index.ps1 -Collection -ThemesOnly` and the
result is committed here. A change to a theme goes to the CabinetOS
repository first; the index is rebuilt and pushed after it.

Plugins and Tool Extensions will be listed the same way once the first
public ones exist. Until then, open an issue in the CabinetOS repository to
propose one.
