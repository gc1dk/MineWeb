# MineWeb — Project Gc_Mc

> **Status: work in progress — !coming soon!**
>
> Nothing here is playable yet. This repository is where the project is being
> built; a proper release lands when the first frame does.

## What is this?

MineWeb is a browser port of the real Minecraft Java Edition client. It is not
a clone and not a reimplementation: the actual client bytecode is transpiled to
JavaScript and run in a web page, with the windowing, input, GPU and audio
layers re-hosted on browser APIs.

- **What you get:** the real client, running on WebGL2 from a static site —
  no install, no Java runtime on the page.
- **What makes it possible:** TeaVM compiles the client's JVM bytecode to
  JavaScript; a hand-written platform layer (SDL, LWJGL bindings, stb,
  audio) bridges Minecraft's native call surface onto the browser.
- **What you need to run it:** a WebGL2-capable browser. That's it.

Minecraft is a trademark of Mojang Synergies AB. This is an unofficial fan
project, not affiliated with or endorsed by Mojang or Microsoft, and it is
intended for people who own the game.

## Roadmap

| Stage | Goal | State |
| ----- | ---- | ----- |
| 1 | Toolchain: TeaVM transpile pipeline, resource tree over HTTP, storage | done |
| 2 | WebGL2 render backend (GL 3.3 path, GPU memory, textures, frame loop) | done |
| 3 | Windowing: SDL/event shim, keyboard, mouse, pointer lock, text input | in progress |
| 4 | **First rendered frame** (`frameCount > 0`) in headless verify | ← we are here |
| 5 | Title screen → main menu playable in a real browser | next |
| 6 | Sound (WebAudio), resource packs, save/load via IndexedDB | planned |
| 7 | Performance pass versus known browser client baselines | planned |
| 8 | Signed Android APK packaging | planned |

Progress is posted as it happens. No fixed date — it's done when it's done.

## Creator

**Gc.idk (aka Gc1dk)** — project creator and maintainer.

## License

The project code is licensed under the **MIT License** — see
[LICENSE](LICENSE). Full license text and any third-party notices ship with
the actual release, not before; see the roadmap notes above.
