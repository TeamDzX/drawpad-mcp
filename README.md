# DrawPad MCP

> **This repository** is where DrawPad MCP is released and supported:
> `DrawPad.mcpb` for Claude Desktop is on the
> [Releases](https://github.com/TeamDzX/drawpad-mcp/releases) page, and bugs
> and requests go in [Issues](https://github.com/TeamDzX/drawpad-mcp/issues).
> All of Opticell's free tools for Claude: [opticell-mcp](https://github.com/TeamDzX/opticell-mcp).

Let Claude design things you can 3D-print. Ask for *"a keychain that says
LUNA"*, *"a 60 mm star cookie cutter"* or *"a plant label for basil"*. Claude
builds it with the engine from **DrawPad Pro.stl**, shows you a preview, and
saves a watertight STL for your slicer plus a DrawPad project you can keep
editing on iPad.

macOS (Apple silicon and Intel).

## Install

**Claude Desktop:** download `DrawPad.mcpb` from
https://www.opticell-limited.com/drawpad and double-click it.

**Claude Code**

```sh
claude mcp add drawpad -- npx -y @opticell/drawpad-mcp mcp
```

**Any other MCP client:** run `npx -y @opticell/drawpad-mcp mcp` as a stdio server.

## What Claude can do

- **Templates:** keychain, cookie cutter (heart, star, circle, flower, cloud or
  any outline), name sign, coaster, gift tag, stencil.
- **Custom designs:** circles, rectangles, polygons, stars, hearts and text,
  with holes, stacked layers and thin walls, all in millimetres.
- **Check an STL:** size, volume, filament weight, and whether it's watertight.

Every design reports its size, volume and grams of PLA/PETG, and comes with a
rendered preview. Files go to `~/Documents/DrawPad Designs`.

## Open designs in DrawPad Pro.stl

AirDrop the `.lsproj` file to your iPad or iPhone, or save it to iCloud Drive,
and open it. DrawPad imports it as a new project, and templates stay editable.
