# Releasing 2.0.0

The order matters: the registry checks the npm package and the `.mcpb` hash
when it accepts `server.json`.

1. Notarise the build: `Tools/drawpad-dist/build.sh` with a notarytool profile.
   Without that, Gatekeeper blocks the binary inside a downloaded `.mcpb`.
2. `npm publish dist/opticell-drawpad-mcp-2.0.0.tgz` (as opticell_limited).
3. `gh release create v2.0.0 dist/DrawPad.mcpb -R TeamDzX/drawpad-mcp`
4. Put `shasum -a 256 dist/DrawPad.mcpb` into `fileSha256` in `server.json`,
   then commit.
5. Make the repo public, then run **Actions → Publish to MCP Registry**.
6. Add a DrawPad row to the MCP servers table in
   [opticell-mcp](https://github.com/TeamDzX/opticell-mcp) and in the TeamDzX profile README.
