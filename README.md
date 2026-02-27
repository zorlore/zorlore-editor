# zorlore-editor

This is the Zorlore world editor

## Runtime Dependencies (Per OS)

These are runtime requirements for the editor executable from `editor/` artifacts.

### Linux (Ubuntu/Debian)

Install:

```bash
sudo apt-get update
sudo apt-get install -y \
  libx11-6 libxcursor1 libxrandr2 libxinerama1 libxi6 libxxf86vm1 \
  libgl1 libasound2
```

Notes:
- The editor uses an OpenGL/X11 runtime stack (Ebiten).
- If audio is not needed, `libasound2` can be omitted.

### macOS

No additional package manager dependencies are typically required for runtime.

Notes:
- The artifact is built for native macOS targets.
- If Gatekeeper blocks launch, remove quarantine attributes or sign/notarize in your distribution flow.

### Windows

No additional runtime packages are typically required for the provided build.

Notes:
- The Windows artifact is built with `CGO_ENABLED=0` for simpler deployment.
- Standard graphics drivers (OpenGL capable) are still required.

## Included Files

- `zorlore-editor` (or `zorlore-editor.exe`)
- `autoborder-spec.json` (when present in source at build time)

Keep `autoborder-spec.json` next to the executable if your workflow depends on autoborder behavior.

These artifacts are produced by CI from `editor/` on every push to `main`.
