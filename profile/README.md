<p align="center">
  <img src="./assets/alopex-banner.svg" alt="Alopex Games" width="100%">
</p>

We are building the foundation for independent virtual worlds that can exist
on their own and still connect to something larger.

A world keeps its rules, simulation, assets, economy, and infrastructure.
Shared protocols handle identity, discovery, presence, and travel between
compatible worlds. Creators decide what crosses those boundaries.

## What we are building

Our first project is a runtime and network model for connected virtual worlds.
The runtime executes each world; a separate control plane helps players find
and enter them.

```text
                         Alopex network
                 identity · discovery · presence
                              │
              ┌───────────────┼───────────────┐
              │               │               │
           World A         World B         World C
           own rules       own rules       own rules
           own server      own server      own server
```

The runtime and authoritative world servers are being designed in C++. SDL3
provides the platform layer, while Lua gives world creators a stable scripting
surface. Elixir coordinates identity, world discovery, presence, and sessions
outside the real-time simulation path.

## Principles

- Worlds remain independent by default.
- Portability is an explicit agreement between worlds.
- Real-time simulation belongs on the world server.
- Creators extend worlds through data and scripts instead of unstable binary
  plugins.
- A small working world is worth more than a large speculative engine.

## Current state

The project is at the architecture stage. We are defining the runtime boundary,
the world package format, and the smallest complete journey: enter one world,
cross a portal, and arrive in another with the same identity.

Development will be public once the first architectural proof is ready.
