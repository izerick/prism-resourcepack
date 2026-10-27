# IzeCraft Network Resource Pack

Global resource pack for the IzeCraft Lobby and Survival servers.

## Compatibility update — 2026-10-26

- Isolate native body effects from the legacy emote UV remapper in the Minecraft 26.3 overlay.
- Filter duplicate sprite registrations and add particle texture aliases to affected models in that overlay.
- Preserve the effective assets of the previous pack for formats 22 through 96, including Minecraft 1.21.8.

Current ZIP SHA-1: `1478c523c56baf1ed2ee760cba55120b78da9b6c`.

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


## Ordinary player/NPC skin compatibility — 2026-10-27

Disable the retired ItemsAdder emote UV remapper in the format-97 entity vertex shader. Ordinary player and NPC skins now keep native UVs regardless of batch vertex indices; native body-effect marker detection and the RGB animation fragment shader remain unchanged. All nonvertex assets and effective formats 22–96 are byte-identical. The 37 entity/armor/OIT/glint variants compile and link to Vulkan SPIR-V. See `source/skin-compat-26.3-validation.json`.

## Shared Survival market controls — 2026-10-27

Trade and PlayerAuctions retained the Skyblock menu configuration, so their UI controls are shared resources needed by Survival. Restore only the 15 trade/auction book controls and their original small textures, with clean model declarations that reference the actual texture paths. Restore the invisible BARRIER/1 menu hit target. All modern book definitions include low-CMD controls without replacing their 50000+ Oraxen branches; legacy overrides are restored too.

The ZIP grows by 56,557 bytes to 12,335,011 bytes. Shaders, player-head transformations, font providers, world models and body effects remain byte-identical. No boss, world or paused-mode plugin is enabled. The backend menu update also removes the nonexistent `custom:avatar` item model, uses recovered confirmation icons, makes money/XP controls explicit and translates the main menu text. See `source/market-menu-compat-validation.json`. In-client menu confirmation remains separate from structural validation.

The recovered sprites are registered explicitly in all four effective block atlases, including the format-97 override, so modern clients can resolve them when baking the GUI models.


## Shared friends menu — 2026-10-27

Restore the BOOK/4 friends/requests control and BOOK/68 empty-list icon used by IzeFriends in Lobby and Survival. Their original small textures are registered in all four effective atlases; legacy and modern dispatches preserve the trade/AH fixes and Oraxen branches. The existing friends/confirmation backgrounds, native player heads, fonts, shaders and backend friendships remain unchanged. The ZIP grows by 1,642 bytes to 12,336,653 bytes. See source/friends-menu-compat-validation.json.

