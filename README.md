# IzeCraft Network Resource Pack

Global resource pack for the IzeCraft Lobby and Survival servers.

## Compatibility update — 2026-10-26

- Isolate native body effects from the legacy emote UV remapper in the Minecraft 26.3 overlay.
- Filter duplicate sprite registrations and add particle texture aliases to affected models in that overlay.
- Preserve the effective assets of the previous pack for formats 22 through 96, including Minecraft 1.21.8.

Current ZIP SHA-1: `54b27056bd8b809d61427fa998ed3efc81b4428c`.

This pack is delivered globally by the network proxy. Backend resource-pack auto-dispatch is disabled so switching game modes can retain the already loaded pack.

## Survival branding — 2026-10-26

Pause and transfer screens now show only SURVIVAL under the existing IZERICK wordmark. The editable SVG source is in `source/pause-survival.svg`. Resource-pack names were updated in every language; gameplay models, shaders, fonts and version overlays remain unchanged.

## Menu-head compatibility — 2026-10-26

Apply the native Minecraft 26.3 skull transformation to special player-head item definitions, including the ModelEngine namespace. Earlier resource formats, menu actions, geometry, shaders and native body effects remain unchanged.
