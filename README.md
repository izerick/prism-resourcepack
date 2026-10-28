# IzeCraft Network Resource Pack

Global resource pack for the IzeCraft Lobby and Survival servers.

## Compatibility update — 2026-10-26

- Isolate native body effects from the legacy emote UV remapper in the Minecraft 26.3 overlay.
- Filter duplicate sprite registrations and add particle texture aliases to affected models in that overlay.
- Preserve the effective assets of the previous pack for formats 22 through 96, including Minecraft 1.21.8.

Current ZIP SHA-1: `2e9d00be309c9ca94c01a23a4450ddf1125ee527`.

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


## Survival AuraSkills parchment menus — 2026-10-27

Restore the 12 original skill progression/navigation controls (BOOK/5–16) and nine skill icons (BONE/1–9), with clean canonical texture references, legacy/modern item dispatches and all four effective block atlases. Existing Oraxen, trade, auction, friends, shader, font and native head/body assets remain unchanged. The ZIP grows by 17,670 bytes to 12,354,323 bytes.

Five Survival menus now use the original Prism parchment design with repaired component references, nine enabled skills in a 3×3 layout, and Spanish labels. Skill configuration, XP sources, rewards, levels and player data are retained. The user confirmed the main and progression menus align correctly. This does not activate Skyblock, dungeons or RPG equipment. See `source/skills-survival-validation.json`.


## Survival Guild Adventures — 2026-10-27

Restore the selected dungeon, forge, ancient-enchantment and ascension resources: 77 carrier/CMD assignments, four worn equipment families, three custom ore textures, both Draedon variants and the sounds used by the selected content. All four effective block atlases and the legacy/modern dispatches use canonical texture references. ModelEngine dispatches follow the actual Survival cache; recycled IDs 6 and 9 replace obsolete lightning bones absent from the current engine output. Existing aura definitions, cosmetics and unrelated carrier branches remain available.

The global ZIP is 16,854,575 bytes, 4,500,252 bytes above the previous skills pack. Existing skin shaders, fonts, native skull transforms and body-effect resources are byte-identical. The server integration uses Survival skills and currency, with independent adventure progression and protected ore nodes. Skyblock and Prison remain paused. Automatic and native-client transaction checks passed; appearance in the owner's clients is tracked separately. See `source/adventures-survival-validation.json`.


## Survival services and enchantment portraits — 2026-10-27

Restore only PLAYER_HEAD/16 to its original 3x3 portrait display, with an exact cutoff at 17 in every legacy and modern dispatch. The native format-97 skull transformation stays intact. Ordinary heads, skin shaders, fonts, body effects and the other models remain unchanged. The three portraits were checked in Minecraft 26.3 and appear complete and centered. The global ZIP is 16,811,424 bytes.

RPG services now use unused buildings in the existing Survival spawn, and the thirteen special ore nodes use the existing resource mine. The imported Skyblock city is archived and no longer loaded. Original NPCs, player progression and existing region rules are preserved. See `source/survival-service-head-validation.json`.


## Survival Guild extras — 2026-10-27

Add selective backpack icons and worn models, thirty stored-tool models, thirteen sound aliases, seven independent Spanish UI backgrounds and the three expedition bosses. New models use reserved IDs and a separate namespace; existing skin shaders, font providers and player-head files stay byte-identical. All effective dispatch branches have reset boundaries and all four atlases include the new sprites. 103 models and their references were validated.

The global ZIP is 20,148,125 bytes (+3,336,701), SHA1 `23b0a005f8e460f331f895e2f63360ce25eb9157`. It remains one global pack without forced downloads between backends. The Survival integration adds a 70-level pass, permanent profession reputation, backpacks, capped wilderness encounters and three routes within one additional native dungeon template. 29 inventory/reputation/encounter checks and 48 route/group/finish checks passed in the isolated native server. Production model IDs match all 64 new bones. Visual confirmation is pending because Computer Use was stopped by Escape. See `source/survival-extras-validation.json`.


## Original Guild interfaces and expedition access — 2026-10-27

Restore the selected original adventure-pass, profession portrait/progress and expedition-selection artwork with Spanish labels. Source UI and keys use a separate namespace and reserved FEATHER models. The global ZIP is 20,368,877 bytes (+220,752), SHA1 `b1f4291551ea8b07ddf93d48e67ac629a4f212d5`. All source references and legacy/modern model cutoffs were independently validated. Existing native heads, skin shaders, old font providers and unrelated assets remain byte-identical.

Survival now validates a key for every expedition participant before readiness and consumes one only at actual dungeon start. Native locksmith recipes provide the three keys; the original Laboratory access stays separate. Mapped exploration chests reveal five common rewards and one rare reward sequentially, with independent persistent claims per player. Closing/reopening does not reroll rewards; full inventory retains unclaimed loot and collected items survive leaving. `/spawn` and the expedition menu use the native dungeon exit. Existing progression, recipe entries and SQLite data remain in place.

26 native checks and two actual-client inventory checks passed in the isolated server. Visual alignment in the owner's client remains pending. See `source/survival-fidelity-validation.json`.

## Native pixel lettering restored — 2026-10-27

The owner reported blurred lettering in the new Guild interfaces. Replace system-font raster text with the existing accepted pixel alphabet from the earlier Survival UI correction. Six source panels, 210 pass-number textures and seven independent menu headers now draw solid pixels directly at their final size. Existing artwork translucency is preserved. All 223 texture dimensions remain unchanged; every other ZIP entry, including shaders, font definitions, models, controls and native heads, is byte-identical.

The global ZIP is 20,308,639 bytes, 60,238 bytes smaller than the previous release, SHA1 `48fb89da24a224fb08772bba1b878fe0d9943666`. No backend restart or gameplay/data changes. The file checks and enlarged pixel previews passed; native-client visual confirmation remains pending. See `source/survival-crisp-text-validation.json`.
