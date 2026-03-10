# ZorLore Editor

The ZorLore Editor is the world-building application for the ZorLore MMORPG stack. It is designed for building a complete online world: map layout, cities, houses, depots, raids, monster spawns, NPCs, items, actions, spells, and even sprite work.

It is not just a map painter. It is the production toolchain for shaping how your MMORPG plays, looks, and evolves.

## Download

Download the latest editor builds here:

- [ZorLore Editor Releases](https://github.com/zorlore/zorlore-editor/releases)

## What You Can Do With It

- Build and edit the world map directly
- Manage cities, start locations, depots, and house layouts
- Configure monster spawns, raids, NPCs, actions, and spells
- Edit item/object definitions and sprite metadata
- Paint, transform, outline, and refine sprites in the built-in sprite editor
- Preview overlays such as raids, lighting, protection zones, and stacked world levels

## Build Your World

The editor is built to let you work on an MMORPG as a world, not as disconnected files.

![World Overview](https://zorlore.com/assets/world-rookgaard-baseline.png)

You can move from terrain to gameplay systems in one workflow: place tiles, define cities, wire up depots, script raid behavior, configure objects, and keep the whole worldpack consistent.

## Overlays And World Debugging

The editor can visualize gameplay-relevant map layers and debugging overlays directly inside the world view.

![Overlay Lighting](https://zorlore.com/assets/overlay-lighting.png)

![Raid Overlay](https://zorlore.com/assets/overlay-raid-thais-orc-invasion.png)

This makes it practical to inspect live gameplay concerns such as raid coverage, floor visibility, lighting, and protected areas without switching tools.

## Sprite Editing

The built-in sprite editor lets you work directly on item appearances without leaving the editor. You can import sprite sheets, slice assets, edit pixels, manipulate full appearances, and tune visuals as part of the same workflow you use to build the map.

![Sprite Editor](https://zorlore.com/assets/sprite-editor.png)

This is useful when you are iterating on custom content and want to adjust how an item or object looks immediately in context.

## Included Files

- `zorlore-editor` or `zorlore-editor.exe`
- `autoborder-spec.json`

Keep `autoborder-spec.json` next to the executable if your workflow depends on autoborder behavior.

## Runtime Dependencies

These are runtime requirements for the editor executable distributed through the release artifacts.

### Linux (Ubuntu/Debian)

Install:

```bash
sudo apt-get update
sudo apt-get install -y \
  libx11-6 libxcursor1 libxrandr2 libxinerama1 libxi6 libxxf86vm1 \
  libgl1 libasound2
```

Notes:
- The editor uses an OpenGL/X11 runtime stack through Ebiten.
- If audio is not needed, `libasound2` can usually be omitted.

### macOS

No additional package manager dependencies are typically required for runtime.

### Windows

No additional runtime packages are typically required for the provided build.

Notes:
- The Windows artifact is built with `CGO_ENABLED=0` for simpler deployment.
- Standard graphics drivers with OpenGL support are still required.

## Documentation

Platform documentation is available here:

- [ZorLore Documentation](https://github.com/zorlore/documentation)

If you want setup and platform-level guidance, start there.
