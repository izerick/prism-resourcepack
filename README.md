# IzeCraft Network Resource Pack

Global resource pack for the IzeCraft Lobby and Survival servers.

## Compatibility update — 2026-10-26

- Isolate native body effects from the legacy emote UV remapper in the Minecraft 26.3 overlay.
- Filter duplicate sprite registrations and add particle texture aliases to affected models in that overlay.
- Preserve the effective assets of the previous pack for formats 22 through 96, including Minecraft 1.21.8.

Current ZIP SHA-1: `94a96c2b5879b4698be26a2ed7b5dd15eb636acf`.

This pack is delivered globally by the network proxy. Backend resource-pack auto-dispatch is disabled so switching game modes can retain the already loaded pack.

## Survival branding — 2026-10-26

Pause and transfer screens now show only SURVIVAL under the existing IZERICK wordmark. The editable SVG source is in `source/pause-survival.svg`. Resource-pack names were updated in every language; gameplay models, shaders, fonts and version overlays remain unchanged.

## Menu-head compatibility — 2026-10-26

Apply the native Minecraft 26.3 skull transformation to special player-head item definitions, including the ModelEngine namespace. Earlier resource formats, menu actions, geometry, shaders and native body effects remain unchanged.


## Lobby and Survival optimization — 2026-10-26

The download ZIP is reduced from 34,782,795 to 12,279,170 bytes (64.7%). Resources belonging to paused modes are held in a separate recovery library. The four complete aura families, active ModelEngine internals, shared fonts/icons, Oraxen/HMCCosmetics assets, shaders and the native 26.3 menu-head fix are preserved. PNG recompression preserves every pixel and ancillary color/transparency chunk.

All retained models and item branches were checked across formats 22–97 and the declared upper bound. No previously available dependency becomes missing. This is structural compatibility validation, not a gameplay benchmark on every client.

Restore the archived modules or rebuild the full pack before enabling Skyblock or Prison. Reuse a specific module by merging its resources and carrier branches, then installing the matching backend blueprint and skills. The private recovery library and original full ZIP are saved locally and on the server; the repository history also contains the previous full pack.

The final cleanup also removes item definitions belonging to inactive ModelEngine assets and preserves the engine player-skin templates. Vanilla base models are used for archived item branches instead of stale texture aliases.

The shared noteblock ore models are retained because Minecraft generates item-context wrappers from blockstates. The dependency checks include those blockstate references.
