# Awesome Game Skill

> 精选的 AI 游戏开发 Agent Skill、MCP 与工具合集  
> *A curated list of AI game-dev agent skills, MCP servers and tools.*

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re) ![entries](https://img.shields.io/badge/entries-255-blue) [![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](LICENSE)

这个列表收集能让 Claude Code、Codex、Cursor、Kimi 等 AI 编程 Agent 更会做游戏的 Skill（SKILL.md）、MCP 服务器和配套工具，覆盖 Unity / Unreal / Godot / Bevy / Roblox 等引擎，以及美术资产、像素风格、音效、测试与逆向。所有链接都经过可访问性检查，星数和许可证来自 GitHub API（2026-10-26 更新）。

- 姐妹仓库：[awesome-kimi-k3-game](https://github.com/gdfsdjj145/awesome-kimi-k3-game) — Kimi K3 做游戏的可玩效果与提示词
- 在线浏览：[gameskill.dev](https://gameskill.dev)
- 机器可读数据：[`data/skills.json`](data/skills.json)

## 目录 / Contents

- [合集与插件 / Collections & Plugins](#合集与插件--collections--plugins)（23）
- [通用系统 / 路由 / General & Routing](#通用系统--路由--general--routing)（28）
- [游戏设计与玩法 / Game Design & Gameplay](#游戏设计与玩法--game-design--gameplay)（21）
- [Unity / Unity](#unity--unity)（25）
- [Unreal / Unreal](#unreal--unreal)（15）
- [Godot / Godot](#godot--godot)（22）
- [Bevy / Bevy](#bevy--bevy)（9）
- [Roblox / Roblox](#roblox--roblox)（9）
- [其他引擎与 Web / Other Engines & Web](#其他引擎与-web--other-engines--web)（12）
- [美术资产与角色 / Art Assets & Characters](#美术资产与角色--art-assets--characters)（72）
- [美术风格与像素 / Art Styles & Pixel Art](#美术风格与像素--art-styles--pixel-art)（3）
- [音效 / Audio](#音效--audio)（5）
- [测试、逆向与发布 / Testing, RE & Release](#测试逆向与发布--testing-re--release)（11）
- [贡献指南 / Contributing](#贡献指南--contributing)
- [许可证 / License](#许可证--license)

## 合集与插件 / Collections & Plugins

| 名称 | 说明 | ★ | 许可证 |
|---|---|---|---|
| [Claude-Code-Game-Studios（合集）](https://github.com/Donchitos/Claude-Code-Game-Studios) | Turn Claude Code into a full game dev studio — 49 AI agents, 72 workflow skills, and a complete coordination system mirroring real studio hierarchy. | 27,558 | MIT |
| [universal-modder（合集）](https://github.com/rehan-remade/universal-modder) | Point Claude at any game: skills, tools and the fal MCP that let Claude Code mod almost any PC game you own — recon, reverse engineering, fal-generated art/3… | 8,962 | MIT |
| [awesome-gamedev-agent-skills（合集）](https://github.com/gamedev-skills/awesome-gamedev-agent-skills) | 74 game-dev skills for AI coding agents — Godot, Unity, Unreal, Phaser, PixiJS, three.js, Bevy, pygame, LÖVE, Roblox. | 4,334 | Apache-2.0 |
| [sprite-gen（合集）](https://github.com/aldegad/sprite-gen) | Generate clean 2D game sprites & animation atlases — component-row pipeline: state rows, alpha cleanup, frame extraction, runtime atlases. | 3,037 | Apache-2.0 |
| [unreal-engine-skills-for-claude-code-plugin（合集）](https://github.com/EpicGames/unreal-engine-skills-for-claude-code-plugin) | （SKILL.md 无 description） | 1,667 | MIT |
| [skills（合集）](https://github.com/Unity-Technologies/skills) | A collection of reusable skills for AI coding agents — prompts, slash commands, and tools built for Unity workflows | 1,148 | 未声明（根目录无 LICENSE） |
| [skills（合集）](https://github.com/scenario-labs/skills) | Get production-ready images, video, audio, and 3D from any AI agent: skills that pick the right model, price before spending, and keep characters and brands … | 1,134 | MIT |
| [GameFactory-3A（合集）](https://github.com/OpenDCAI/GameFactory-3A) | Open-source 3A game-generation skill and asset framework; 10 agent SKILL.md files for asset QA (3D object, 3D scene, audio, CG video) and more. | 963 | Apache-2.0 |
| [novel-to-game（合集）](https://github.com/zenstory-ai/novel-to-game) | Agent skills for source-grounded novel-to-game adaptation (小说改编游戏 / story to game): cited design docs, target-runtime builds, evidence-based QA. | 924 | MIT |
| [3dviz-pro-max（合集）](https://github.com/viettranx/3dviz-pro-max) | Agent skill for creative 3D visualization: turn an idea into a Three.js/Blender scene worth exploring. | 902 | MIT |
| [Game-Dev-Agentic-Skills（合集）](https://github.com/thedivergentai/Game-Dev-Agentic-Skills) | Multi-engine long-term memory for game AI agents. | 892 | LGPL-3.0 |
| [blender-skills（合集）](https://github.com/EL4CTEO/blender-skills) | Professional Blender 5.2 workflows as Agent Skills for Claude Code, Codex, Gemini CLI, Copilot and Cursor: modeling, UVs, PBR, baking, rigging, animation, ex… | 507 | MIT |
| [aseprite-ai-artist（合集）](https://github.com/with-pebbly/aseprite-ai-artist) | Your coding agent paints pixel art in the Aseprite window you already have open. | 476 | MIT |
| [unreal-engine-skills（合集）](https://github.com/quodsoler/unreal-engine-skills) | Unreal Engine C++ skills for AI coding agents. | 405 | MIT |
| [pixel-path（合集）](https://github.com/jonwheatley/pixel-path) | Turn any two places into a pixel-art fly-through of the real road. | 263 | MIT（LICENSE 文件） |
| [hermes-plugin-gameforge（GameForge，合集）](https://github.com/DECRUX9812/hermes-plugin-gameforge) | Game development plugin for Hermes Agent: sound effects, music, NPC voices, pixel art, 3D models, Godot/Unity/Blender/Unreal, a playtester that actually play… | 41 | MIT |
| [mobile-ai-agents](https://github.com/salmanashraf/mobile-ai-agents) | Mobile AI skills, agents and workflows for Android, iOS, Flutter, React Native, Unity and Unreal apps and games | 32 | MIT |
| [game-superpowers](https://github.com/mike007jd/game-superpowers) | skills 优先的游戏开发合集：构建、审计、打磨、产品化游戏项目 | 21 | MIT |
| [ForgeSkills（合集）](https://github.com/sekaikx/ForgeSkills) | 开源 AI 游戏开发 skill 合集：玩法系统、程序化建模、参考图还原、动画、移动、镜头、灯光、贴图、VFX、调试、性能、Godot 管线与 Blender 无头模式，带总调度 orchestrator | 14 | Apache-2.0 |
| [FunplayAI/funplay-skill（合集）](https://github.com/FunplayAI/funplay-skill) | Open-source game development skills: reusable workflows for texture processing, audio, level generation, asset optimization, Cocos UI retrofit and more. | 10 | MIT |
| [open-game-skills（合集）](https://github.com/jammyfu/open-game-skills) | Open-source agent skill cluster for games: engine-neutral feel/camera/combat + studio presets (Nintendo/Zelda, Capcom, Konami, Blizzard, indie) + Three.js/Pi… | 8 | MIT |
| [skills-gamedev（合集）](https://github.com/poorvith-mp/skills-gamedev) | 26 agent skills for game development: Unity, Unreal Engine 5, Blender modeling, shaders, and audio pipelines. | 5 | MIT |
| [blender-unity-game-studio（合集）](https://github.com/phytrisha/blender-unity-game-studio) | Claude Code 游戏工作室模板（Unity 6 + Blender）：44 个 agent、80 个 skill，带脚本化的 Blender 到 Unity 3D 美术管线，基于 Claude Code Game Studios | 0 | MIT |

## 通用系统 / 路由 / General & Routing

| 名称 | 说明 | ★ | 许可证 |
|---|---|---|---|
| [balance-check](https://github.com/Donchitos/Claude-Code-Game-Studios/tree/main/.claude/skills/balance-check) | Find balance outliers, broken progressions, degenerate strategies, economy imbalances in formulas and data. | 27,558 | MIT |
| [brainstorm](https://github.com/Donchitos/Claude-Code-Game-Studios/tree/main/.claude/skills/brainstorm) | Guides the user through finding and choosing a game concept. | 27,558 | MIT |
| [launch-checklist](https://github.com/Donchitos/Claude-Code-Game-Studios/tree/main/.claude/skills/launch-checklist) | Launch readiness across every department: code, content, store, marketing, community, infrastructure, legal, go/no-go sign-offs. | 27,558 | MIT |
| [localize](https://github.com/Donchitos/Claude-Code-Game-Studios/tree/main/.claude/skills/localize) | Localization pipeline — find hardcoded strings, extract string tables, cultural review, VO, RTL, enforce string freeze. | 27,558 | MIT |
| [map-systems](https://github.com/Donchitos/Claude-Code-Game-Studios/tree/main/.claude/skills/map-systems) | Decompose a concept into individual systems, map dependencies, prioritize design order, create the systems index. | 27,558 | MIT |
| [prototype](https://github.com/Donchitos/Claude-Code-Game-Studios/tree/main/.claude/skills/prototype) | Concept prototype before GDDs — throwaway HTML, Engine or Paper build, PROCEED/PIVOT/KILL/NOT ASSESSED. | 27,558 | MIT |
| [quick-design](https://github.com/Donchitos/Claude-Code-Game-Studios/tree/main/.claude/skills/quick-design) | Lightweight spec for small changes — tuning adjustments, minor mechanics. | 27,558 | MIT |
| [team-combat](https://github.com/Donchitos/Claude-Code-Game-Studios/tree/main/.claude/skills/team-combat) | Orchestrate the combat team — game-designer, gameplay-programmer, ai-programmer, technical-artist, sound-designer, qa-tester — design through implement and v… | 27,558 | MIT |
| [router](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/router) | Routes any game-development request to the right specialized skill(s): it detects the engine (Godot, Unity, Unreal, Bevy, Phaser, PixiJS, three.js, LÖVE, pyg… | 4,334 | Apache-2.0 |
| [ai-behavior-trees-utility-ai](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/disciplines/ai-behavior-trees-utility-ai) | Build a production behavior-tree runtime (Blackboard, action/condition leaves, sequence/selector/parallel composites, decorators) and a Utility AI system (re… | 4,334 | Apache-2.0 |
| [camera-systems](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/disciplines/camera-systems) | Build game cameras that feel good — 2D follow with a deadzone, look-ahead, smoothing, and level-bounds clamping; 3D third-person orbit with collision and fir… | 4,334 | Apache-2.0 |
| [dialogue-systems](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/disciplines/dialogue-systems) | Build branching dialogue and narrative — a node/choice graph with conditions, variables, and localization hooks — and choose between authoring tools Ink and … | 4,334 | Apache-2.0 |
| [game-ai](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/disciplines/game-ai) | Design NPC and enemy decision-making with finite state machines, behavior trees, steering behaviors, and A* pathfinding — engine-neutral algorithms that pair… | 4,334 | Apache-2.0 |
| [game-ui-ux](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/disciplines/game-ui-ux) | Design and build game UI/UX — HUDs, menus, and overlays — that survive every screen: anchor- based responsive layout, resolution/aspect scaling and safe area… | 4,334 | Apache-2.0 |
| [input-systems](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/disciplines/input-systems) | Architect game input — action mapping (abstracting keys into named actions), rebinding with conflict detection and persistence, multi-device support (keyboar… | 4,334 | Apache-2.0 |
| [physics-tuning](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/disciplines/physics-tuning) | Tune game physics for stable, good-feeling motion — fixed vs variable timestep, render interpolation, mass/gravity/drag, continuous collision detection (CCD)… | 4,334 | Apache-2.0 |
| [save-systems](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/disciplines/save-systems) | Design save/load for game state — choosing what to serialize, file formats, save slots, atomic crash-safe writes, schema versioning and migration, and autosave. | 4,334 | Apache-2.0 |
| [coop-anything](https://github.com/cranebeaker/coop-anything) | 让 AI agent 把任意单机游戏改成可联机/分屏合作：MCP 服务 + playbook，负责逆向、修复、实机测试和打包分享 | 1,380 | MIT |
| [scenario-zbrush-character-creature](https://github.com/scenario-labs/skills/tree/main/skills/dcc/zbrush/scenario-zbrush-character-creature) | Use when sculpting a realistic head, face, portrait, body or creature in ZBrush (anatomy, landmarks, proportions, "the face looks off", eyes, lips, jaw), add… | 1,134 | MIT |
| [scenario-zbrush-stylized](https://github.com/scenario-labs/skills/tree/main/skills/dcc/zbrush/scenario-zbrush-stylized) | Use when sculpting a stylized or cartoon character, bust, collectible or toy in ZBrush (Overwatch, Fortnite, Disney look), judging shape language (S and C cu… | 1,134 | MIT |
| [brief](https://github.com/with-pebbly/aseprite-ai-artist/tree/main/skills/brief) | Turn a vague pixel-art request into a written brief — size, palette, view, light, outline style — and confirm it with the user before any pixel is drawn. | 476 | MIT |
| [fix](https://github.com/with-pebbly/aseprite-ai-artist/tree/main/skills/fix) | Change a sprite that already exists — the user's own work or your earlier output — without destroying what is already right. | 476 | MIT |
| [Game-Decompilation-Skill-For-Claude](https://github.com/lemiur/Game-Decompilation-Skill-For-Claude) | 给 Claude Code 的游戏字节级匹配反编译 skill 包：逐函数重建可读 C/C++、诊断编译器不匹配、还原原始辅助函数、多 agent 并行协作 | 80 | 未标注 |
| [game-reverse-engineering](https://github.com/DECRUX9812/hermes-plugin-gameforge/tree/main/skills/game-reverse-engineering) | Decompile and analyze game binaries you have rights to. | 41 | MIT |
| [game-design](https://github.com/poorvith-mp/skills-gamedev/tree/main/skills/game-design) | Design systems and mechanics: GDD authorship, gameplay loops, economy balancing and player psychology. | 5 | MIT |
| [game-monetization](https://github.com/poorvith-mp/skills-gamedev/tree/main/skills/game-monetization) | Design free-to-play economies, battle passes and cosmetic shops with anti-predatory guardrails. | 5 | MIT |
| [narrative-design](https://github.com/poorvith-mp/skills-gamedev/tree/main/skills/narrative-design) | Design branching dialogue, lore architecture and environmental storytelling aligned to the GDD. | 5 | MIT |
| [Scorezilla MCP](https://scorezilla.dev/mcp) | 让 Claude Code/Cursor 一句话给游戏接全球排行榜的 MCP 服务：自动建游戏和榜单并给出接入代码，SDK 约 5KB 无依赖，免费 | — | 未标注 |

## 游戏设计与玩法 / Game Design & Gameplay

| 名称 | 说明 | ★ | 许可证 |
|---|---|---|---|
| [team-level](https://github.com/Donchitos/Claude-Code-Game-Studios/tree/main/.claude/skills/team-level) | Orchestrate the level team — level-designer, narrative-director, world-builder, art-director, systems-designer, qa-tester — for complete area creation. | 27,558 | MIT |
| [mod-any-game](https://github.com/rehan-remade/universal-modder/tree/main/.agents/skills/mod-any-game) | Mod a PC game the user owns, taking an idea to working in the real game and recorded. | 8,962 | MIT |
| [game-feel](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/disciplines/game-feel) | Add "juice" and game feel that makes actions satisfying — screen shake, hit-stop/freeze frames, tweened/eased motion, squash & stretch, knockback, and layere… | 4,334 | Apache-2.0 |
| [level-design](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/disciplines/level-design) | Design and build playable levels — the blockout/whitebox-to-playable workflow, player metrics and grid layout, pacing and flow (tension/rest curve), gating a… | 4,334 | Apache-2.0 |
| [procedural-gen](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/disciplines/procedural-gen) | Generate game content procedurally — seeded deterministic RNG, value/Perlin/ Simplex noise for terrain and heightmaps, grid dungeon generation (rooms + corri… | 4,334 | Apache-2.0 |
| [card-game](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/genres/card-game) | Build a card game: card data, deck/hand/discard zones, draw/shuffle/reshuffle, a turn structure, costs, and effect resolution. | 4,334 | Apache-2.0 |
| [fps-shooter](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/genres/fps-shooter) | Build a first-person shooter: move+mouse-look controller, hitscan or projectile shooting, weapons, health, and enemy AI. | 4,334 | Apache-2.0 |
| [platformer](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/genres/platformer) | Build a 2D platformer: run/jump control with coyote time, jump buffering, and variable jump height, plus tiled levels and hazards. | 4,334 | Apache-2.0 |
| [puzzle](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/genres/puzzle) | Build a puzzle game: grid/board state, move input, rule-based resolution (match-3 cascades, sokoban pushes, tile logic), scoring, and undo. | 4,334 | Apache-2.0 |
| [roguelike](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/genres/roguelike) | Build a roguelike: turn-based grid movement, procedural dungeons, permadeath, field-of-view, and loot tables. | 4,334 | Apache-2.0 |
| [rpg](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/genres/rpg) | Build an RPG: stats and leveling, inventory and equipment, quests, branching dialogue, save/load, and combat. | 4,334 | Apache-2.0 |
| [survival-crafting](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/genres/survival-crafting) | Build a survival-crafting game: resource gathering, inventory, crafting and a tech tree, needs (hunger/thirst/temperature), and base building. | 4,334 | Apache-2.0 |
| [tower-defense](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/genres/tower-defense) | Build a tower defense: enemies pathing along lanes, wave spawning, towers that auto-target and fire, an economy, and lives. | 4,334 | Apache-2.0 |
| [visual-novel](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/genres/visual-novel) | Build a visual novel: a branching script, character and background display, a text box with choices, save/load, backlog, and skip/auto. | 4,334 | Apache-2.0 |
| [game-world-design](https://github.com/zenstory-ai/novel-to-game/tree/main/skills/game-world-design) | Design game experience, systems, and levels. | 924 | MIT |
| [novel-game-analyze](https://github.com/zenstory-ai/novel-to-game/tree/main/skills/novel-game-analyze) | Deconstruct a novel for game adaptation. | 924 | MIT |
| [novel-to-game](https://github.com/zenstory-ai/novel-to-game/tree/main/skills/novel-to-game) | Turn a novel into a fully playable game on the selected target platform. | 924 | MIT |
| [game-studio](https://github.com/DECRUX9812/hermes-plugin-gameforge/tree/main/skills/game-studio) | Take a game idea from pitch to a playtested build. | 41 | MIT |
| [build-3d-game-rooms](https://github.com/tabutyn/build-3d-game-rooms) | Open agent skill for designing, auditing, and shipping interactive 3D game rooms. | 8 | MIT |
| [level-design](https://github.com/poorvith-mp/skills-gamedev/tree/main/skills/level-design) | Design layout, pacing, encounter placement and environmental narrative. | 5 | MIT |
| [rapid-game](https://github.com/DAWN47/rapid-game) | 主题驱动的限时游戏开发 skill：7 个玩法模板 + 零依赖 Canvas 微引擎 + 数据驱动换皮，零素材离线可跑 | 0 | 未声明（NOASSERTION） |

## Unity / Unity

| 名称 | 说明 | ★ | 许可证 |
|---|---|---|---|
| [Unity-MCP（IvanMurzak）](https://github.com/IvanMurzak/Unity-MCP) | Unity 的 AI Skills + MCP 工具 + CLI，完整的 AI 开发与测试闭环，任意 C# 方法一行变工具 | 4,530 | Apache-2.0 |
| [Unity-Skills（Besty0728 合集）](https://github.com/Besty0728/Unity-Skills) | AI automation skills for Unity: drive the Unity Editor through a local REST API — scripts, scenes, prefabs, assets, materials, lighting, tests and hundreds o… | 1,890 | MIT |
| [2d-pixel-perfect](https://github.com/Unity-Technologies/skills/tree/main/skills/2d-pixel-perfect) | Sets up, diagnoses, and fixes pixel perfect 2D rendering with PixelPerfectCamera in URP or Built-in. | 1,148 | 未声明（根目录无 LICENSE） |
| [asset-transformer-toolkit](https://github.com/Unity-Technologies/skills/tree/main/skills/asset-transformer-toolkit) | Imports 3D models and point clouds with Asset Transformer Toolkit (formerly Pixyz), and creates, edits, and runs RuleSets, Actions, and LODs. | 1,148 | 未声明（根目录无 LICENSE） |
| [audio-setup-mixers](https://github.com/Unity-Technologies/skills/tree/main/skills/audio-setup-mixers) | Routes Audio Sources into existing Audio Mixer Groups, classifying each source by what it plays. | 1,148 | 未声明（根目录无 LICENSE） |
| [build-gtk](https://github.com/Unity-Technologies/skills/tree/main/skills/build-gtk) | Builds node-based Editor tools with Unity Graph Toolkit (GTK) on Unity 6.6+: graphs, nodes, ports and validation, State Machine API tools on 6.7+, and runtim… | 1,148 | 未声明（根目录无 LICENSE） |
| [build-live-game](https://github.com/Unity-Technologies/skills/tree/main/skills/build-live-game) | Builds and operates live games with Unity Services. | 1,148 | 未声明（根目录无 LICENSE） |
| [create-2d-physics](https://github.com/Unity-Technologies/skills/tree/main/skills/create-2d-physics) | Creates and fixes Unity 2D physics in both systems, 2D Physics Core and the legacy Rigidbody 2D system, for any 2D physics question even if neither is named. | 1,148 | 未声明（根目录无 LICENSE） |
| [create-tile-palette-or-rule-tiles](https://github.com/Unity-Technologies/skills/tree/main/skills/create-tile-palette-or-rule-tiles) | Create a 2D tile palette from sprites or textures, or make tiles change based on their neighbours. | 1,148 | 未声明（根目录无 LICENSE） |
| [generate-editor-search-query](https://github.com/Unity-Technologies/skills/tree/main/skills/generate-editor-search-query) | Generates Unity Search queries and opens the Search window to find assets or scene objects. | 1,148 | 未声明（根目录无 LICENSE） |
| [implement-in-app-purchases](https://github.com/Unity-Technologies/skills/tree/main/skills/implement-in-app-purchases) | Implements, configures, and debugs Unity In-App Purchases, including subscriptions, receipt validation, and direct-to-customer payments via Stripe or Coda. | 1,148 | 未声明（根目录无 LICENSE） |
| [initialize-ai-navigation](https://github.com/Unity-Technologies/skills/tree/main/skills/initialize-ai-navigation) | Sets up and configures Unity AI Navigation, including NavMesh surfaces, agents, obstacles, and links. | 1,148 | 未声明（根目录无 LICENSE） |
| [levelplay-unity-integration](https://github.com/Unity-Technologies/skills/tree/main/skills/levelplay-unity-integration) | Integrates the LevelPlay ad mediation SDK via the Ads Mediation package. | 1,148 | 未声明（根目录无 LICENSE） |
| [localization](https://github.com/Unity-Technologies/skills/tree/main/skills/localization) | Sets up and configures Unity Localization, including locales, String and Asset Tables, and CJK fonts. | 1,148 | 未声明（根目录无 LICENSE） |
| [manage-sprite-atlas](https://github.com/Unity-Technologies/skills/tree/main/skills/manage-sprite-atlas) | Manages SpriteAtlas assets through a prebuild pipeline, covering master and variant atlases, packing settings, and platform overrides. | 1,148 | 未声明（根目录无 LICENSE） |
| [migrate-birp-to-urp](https://github.com/Unity-Technologies/skills/tree/main/skills/migrate-birp-to-urp) | Plans, executes, and troubleshoots migration from the Built-in Render Pipeline to URP. | 1,148 | 未声明（根目录无 LICENSE） |
| [new-unity-project](https://github.com/Unity-Technologies/skills/tree/main/skills/new-unity-project) | Guides creating a new Unity project, gathering concept, platforms, and monetization before setting up the project, source control, and packages. | 1,148 | 未声明（根目录无 LICENSE） |
| [optimize-audio](https://github.com/Unity-Technologies/skills/tree/main/skills/optimize-audio) | Optimizes audio memory, CPU cost, and playback quality through import settings and mixer configuration. | 1,148 | 未声明（根目录无 LICENSE） |
| [optimize-text-mesh-pro](https://github.com/Unity-Technologies/skills/tree/main/skills/optimize-text-mesh-pro) | Optimizes TextMeshPro rendering, memory, and font setup, including font asset stacks, fallback atlases, SDF quality, and worldspace text. | 1,148 | 未声明（根目录无 LICENSE） |
| [optimize-web](https://github.com/Unity-Technologies/skills/tree/main/skills/optimize-web) | Optimizes Unity WebGL and WebGPU builds for smaller downloads and faster load. | 1,148 | 未声明（根目录无 LICENSE） |
| [physics-3d-collision](https://github.com/Unity-Technologies/skills/tree/main/skills/physics-3d-collision) | Diagnoses 3D PhysX collision and trigger problems. | 1,148 | 未声明（根目录无 LICENSE） |
| [project-auditor-fixes](https://github.com/Unity-Technologies/skills/tree/main/skills/project-auditor-fixes) | Instructions for how to use Project Auditor to find and fix a list of issues. | 1,148 | 未声明（根目录无 LICENSE） |
| [unity-agent-plugin（Unity 官方）](https://github.com/Unity-Technologies/unity-agent-plugin) | Unity plugin for third-party agent platforms (official Unity-Technologies); X posts describe it as skills + local Unity CLI without MCP, for Claude/Codex, Un… | 561 | NOASSERTION |
| [unity-dev](https://github.com/DECRUX9812/hermes-plugin-gameforge/tree/main/skills/unity-dev) | Scaffold and batch-build Unity games from GameForge. | 41 | MIT |
| [agent-foundry](https://github.com/furkantokkan/agent-foundry) | 100+ reusable skills for Codex and Claude Code to build Unity games: planning, coding, testing, UI polish, Blender assets, AI 3D | 11 | MIT |

## Unreal / Unreal

| 名称 | 说明 | ★ | 许可证 |
|---|---|---|---|
| [create-toolset](https://github.com/EpicGames/unreal-engine-skills-for-claude-code-plugin/tree/main/skills/create-toolset) | Use this skill when authoring or extending an Unreal Engine toolset, a class of static, AI-callable functions registered with `ToolsetRegistry` and exposed t… | 1,667 | MIT |
| [unreal-mcp](https://github.com/EpicGames/unreal-engine-skills-for-claude-code-plugin/tree/main/skills/unreal-mcp) | Use this skill to perform actions inside an Unreal Engine project via a live-editor MCP connection. | 1,667 | MIT |
| [unreal-skill](https://github.com/EpicGames/unreal-engine-skills-for-claude-code-plugin/tree/main/skills/unreal-skill) | Use this skill when creating, editing, or reviewing an Unreal Engine Agent Skill, a named bundle of instructions registered with the unreal-mcp server (disti… | 1,667 | MIT |
| [ue-actor-component-architecture](https://github.com/quodsoler/unreal-engine-skills/tree/main/skills/ue-actor-component-architecture) | Use when writing or debugging AActor and UActorComponent C++: constructor vs BeginPlay, PostInitializeComponents, EndPlay cleanup, SpawnActor/SpawnActorDefer… | 405 | MIT |
| [ue-ai-navigation](https://github.com/quodsoler/unreal-engine-skills/tree/main/skills/ue-ai-navigation) | Use when writing Unreal Engine C++ AI — AI controllers, behavior tree nodes, blackboards, AI perception, navmesh pathfinding, EQS queries or Smart Objects. | 405 | MIT |
| [ue-animation-system](https://github.com/quodsoler/unreal-engine-skills/tree/main/skills/ue-animation-system) | Use when writing or debugging Unreal Engine animation C++: AnimInstance subclasses, thread-safe update, FAnimInstanceProxy, montage playback and delegates, a… | 405 | MIT |
| [ue-async-threading](https://github.com/quodsoler/unreal-engine-skills/tree/main/skills/ue-async-threading) | Use when offloading work off the game thread, dispatching results back to it, running data-parallel loops, or scheduling timers and tickers in UE C++. | 405 | MIT |
| [ue-audio-system](https://github.com/quodsoler/unreal-engine-skills/tree/main/skills/ue-audio-system) | Use when playing, mixing or debugging sound in Unreal Engine — one-shot SFX, looping ambience, music, dialogue or procedural audio. | 405 | MIT |
| [ue-blueprint-cpp-interop](https://github.com/quodsoler/unreal-engine-skills/tree/main/skills/ue-blueprint-cpp-interop) | Use when exposing C++ to Blueprint or calling Blueprint from C++: UFUNCTION(BlueprintCallable), BlueprintPure, BlueprintImplementableEvent, BlueprintNativeEv… | 405 | MIT |
| [ue-character-movement](https://github.com/quodsoler/unreal-engine-skills/tree/main/skills/ue-character-movement) | Use when writing or debugging UCharacterMovementComponent code: custom movement modes, floor detection, jumping, crouching, root motion, moving platforms, or… | 405 | MIT |
| [ue-cpp-foundations](https://github.com/quodsoler/unreal-engine-skills/tree/main/skills/ue-cpp-foundations) | Use when writing Unreal Engine C++ that touches the reflection system or core types: UCLASS, UPROPERTY, UFUNCTION, USTRUCT, UENUM, GENERATED_BODY, TObjectPtr… | 405 | MIT |
| [ue-data-assets-tables](https://github.com/quodsoler/unreal-engine-skills/tree/main/skills/ue-data-assets-tables) | Use when modelling designer-authored game data in C++ and loading it: data assets, data tables, curve tables, soft references and asset streaming. | 405 | MIT |
| [ue-editor-tools](https://github.com/quodsoler/unreal-engine-skills/tree/main/skills/ue-editor-tools) | Use when extending the Unreal Editor from C++ with detail customizations, editor utility widgets, menus, editor modes, asset definitions or editor subsystems. | 405 | MIT |
| [Vibe3D](https://github.com/kevinpbuckley/Vibe3D) | UE 5.8 程序化 3D 建模 AI 工具集：图元、布尔、放样、UV、烘焙、绑定、碰撞、LOD，走原生 MCP | 14 | MIT |
| [unreal-vibe-modding](https://github.com/glitchbunny0/unreal-vibe-modding) | 通过 UE4SS 让 AI agent 在运行中的 Unreal 游戏里实时跑 Lua 做 mod：CLI、MCP 服务和 agent skills | 0 | MIT |

## Godot / Godot

| 名称 | 说明 | ★ | 许可证 |
|---|---|---|---|
| [godot-2d-movement](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/godot/godot-2d-movement) | Implement 2D kinematic character movement in Godot 4.7 with CharacterBody2D and move_and_slide(): platformer run/jump with gravity, top-down 8-direction moti… | 4,334 | Apache-2.0 |
| [godot-3d-essentials](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/godot/godot-3d-essentials) | Set up a Godot 4.7 3D scene: Node3D transforms, Camera3D, lighting (DirectionalLight3D/OmniLight3D), WorldEnvironment for sky/ambient/tonemap/post, MeshInsta… | 4,334 | Apache-2.0 |
| [godot-animation](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/godot/godot-animation) | Animate in Godot 4.7 three ways: AnimationPlayer for keyframed clips (incl. | 4,334 | Apache-2.0 |
| [godot-audio](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/godot/godot-audio) | Play and mix audio in Godot 4.7: AudioStreamPlayer (2D/3D variants), audio buses with volume/mute and effects, music vs SFX routing, db/linear volume, and pr… | 4,334 | Apache-2.0 |
| [godot-csharp](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/godot/godot-csharp) | Use C#/.NET in Godot 4.7: partial classes extending nodes, the PascalCase lifecycle (_Ready/_Process/_PhysicsProcess), [Export] fields, [Signal] delegates as… | 4,334 | Apache-2.0 |
| [godot-export](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/godot/godot-export) | Export and build a Godot 4.7 project for distribution: install export templates, define export presets (Windows/macOS/Linux/Web/Android), run headless comman… | 4,334 | Apache-2.0 |
| [godot-gdscript-headless-testing](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/godot/godot-gdscript-headless-testing) | Run GDScript test suites from the command line with `godot --headless`, using a SceneTree/MainLoop runner script that exits non-zero on failure so CI can gat… | 4,334 | Apache-2.0 |
| [godot-gdscript](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/godot/godot-gdscript) | Write idiomatic GDScript for Godot 4.7: static typing, the node lifecycle (_ready/_process/_physics_process), @export/@onready/@tool annotations, signals, an… | 4,334 | Apache-2.0 |
| [godot-multiplayer](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/godot/godot-multiplayer) | Build networked games with Godot 4.7 high-level multiplayer: set up an ENetMultiplayerPeer server/client, define RPCs with the @rpc annotation (call via rpc(… | 4,334 | Apache-2.0 |
| [godot-nodes-scenes](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/godot/godot-nodes-scenes) | Structure a Godot 4.7 project with the scene tree and node composition: build reusable scenes, instance PackedScenes at runtime, navigate the tree safely, an… | 4,334 | Apache-2.0 |
| [godot-physics](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/godot/godot-physics) | Use Godot 4.7 physics bodies and detection in 2D and 3D: RigidBody, StaticBody, Area, and CharacterBody; collision layers vs masks; contact/overlap signals; … | 4,334 | Apache-2.0 |
| [godot-resources](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/godot/godot-resources) | Design data-driven Godot 4.7 games with custom Resource classes: define typed data with class_name + @export, save/load .tres/.res files, instance and duplic… | 4,334 | Apache-2.0 |
| [godot-shaders](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/godot/godot-shaders) | Write Godot 4.7 shaders in the Godot Shading Language: canvas_item shaders for 2D and spatial shaders for 3D, with vertex/fragment functions, uniforms (sourc… | 4,334 | Apache-2.0 |
| [godot-signals-groups](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/godot/godot-signals-groups) | Build event-driven, decoupled Godot 4.7 gameplay with signals and node groups: declare and emit custom signals, connect with Callables (incl. | 4,334 | Apache-2.0 |
| [godot-tilemap](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/godot/godot-tilemap) | Build and edit tile-based 2D levels in Godot 4.7 with TileMapLayer and TileSet: paint layers, set up collision/navigation/custom-data on tiles, autotile with… | 4,334 | Apache-2.0 |
| [godot-ui-control](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/godot/godot-ui-control) | Build Godot 4.7 user interfaces with Control nodes: anchors and offsets for responsive layout, Container nodes (VBox/HBox/Grid/Margin) for automatic arrangem… | 4,334 | Apache-2.0 |
| [scenario-godot-2d](https://github.com/scenario-labs/skills/tree/main/skills/game-engines/godot/scenario-godot-2d) | Use when building a 2D game in Godot 4.7: make a platformer or top-down controller that feels right (coyote time, jump buffer, jump height), TileMapLayer and… | 1,134 | MIT |
| [scenario-godot-vfx](https://github.com/scenario-labs/skills/tree/main/skills/game-engines/godot/scenario-godot-vfx) | Use when making or fixing particle effects and game feel in Godot 4.7: GPUParticles3D or GPUParticles2D explosion, fireball projectile with trail, impact, sp… | 1,134 | MIT |
| [gai（godot-fun）](https://github.com/godot-fun/gai) | 用 Godot 写的轻量 AI agent 与 skill 工作流框架 | 194 | MIT |
| [godot-dev](https://github.com/DECRUX9812/hermes-plugin-gameforge/tree/main/skills/godot-dev) | Build, debug and export Godot 4 games headlessly. | 41 | MIT |
| [game-development-skills（LuBolin）](https://github.com/LuBolin/game-development-skills) | 游戏开发 agent skills，含经 Godot 实测的 UI 设计工作流和可运行示例 | 0 | MIT |
| [godot-agent-plugins](https://github.com/dannroda/godot-agent-plugins) | Godot 4 的 Claude Code 插件市场：GDScript 架构、模式、数据、代码审查和 shader skills | 0 | MIT |

## Bevy / Bevy

| 名称 | 说明 | ★ | 许可证 |
|---|---|---|---|
| [bevy-ecs](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/other-engines/bevy-ecs) | Structure a Bevy app around its Entity Component System: build the App with plugins, define Component/Resource types, write systems with Query/Res/Commands, … | 4,334 | Apache-2.0 |
| [bevy-character-movement](https://github.com/thedivergentai/Game-Dev-Agentic-Skills/tree/main/skills/bevy-character-movement) | Bevy 0.20 kinematic character movement: intent components, FixedUpdate integration, coyote time, and jump buffer. | 892 | LGPL-3.0 |
| [bevy-combat-system](https://github.com/thedivergentai/Game-Dev-Agentic-Skills/tree/main/skills/bevy-combat-system) | Bevy ECS combat: Health, Team, and Invuln on actors, Hit messages, melee reach, despawn on FixedUpdate after damage. | 892 | LGPL-3.0 |
| [bevy-dialogue-system](https://github.com/thedivergentai/Game-Dev-Agentic-Skills/tree/main/skills/bevy-dialogue-system) | Bevy 0.20 dialogue data: line tables in a resource, the current line index on a component, and choice flags filtered before the write. | 892 | LGPL-3.0 |
| [bevy-economy-system](https://github.com/thedivergentai/Game-Dev-Agentic-Skills/tree/main/skills/bevy-economy-system) | Bevy ECS economy: Wallet components, a PriceTable resource, Purchase and Transfer messages, vendor stock. | 892 | LGPL-3.0 |
| [bevy-genre-platformer](https://github.com/thedivergentai/Game-Dev-Agentic-Skills/tree/main/skills/bevy-genre-platformer) | Route a Bevy 0.20 platformer: coyote time and jump buffer on Mover, gravity on FixedUpdate, one-way ledges, follow camera. | 892 | LGPL-3.0 |
| [bevy-genre-roguelike](https://github.com/thedivergentai/Game-Dev-Agentic-Skills/tree/main/skills/bevy-genre-roguelike) | Route a Bevy 0.20 roguelike: RunSeed resource, room entities, permadeath flag, turn energy, grid pickup. | 892 | LGPL-3.0 |
| [bevy-genre-tower-defense](https://github.com/thedivergentai/Game-Dev-Agentic-Skills/tree/main/skills/bevy-genre-tower-defense) | Bevy genre router for tower defense. | 892 | LGPL-3.0 |
| [bevy-inventory-system](https://github.com/thedivergentai/Game-Dev-Agentic-Skills/tree/main/skills/bevy-inventory-system) | Bevy ECS skill for inventories. | 892 | LGPL-3.0 |

## Roblox / Roblox

| 名称 | 说明 | ★ | 许可证 |
|---|---|---|---|
| [roblox-characters](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/other-engines/roblox-characters) | Build respawn-safe Roblox character systems around Players, CharacterAdded/CharacterRemoving, Humanoid, HumanoidRootPart, Animator, R6/R15 rigs, movement, an… | 4,334 | Apache-2.0 |
| [scenario-roblox-animation](https://github.com/scenario-labs/skills/tree/main/skills/game-engines/roblox/scenario-roblox-animation) | Use when animating Roblox characters, NPCs or creatures: animation not playing, wrong animation wins, animation priority or weight, blending, animation event… | 1,134 | MIT |
| [scenario-roblox-assets](https://github.com/scenario-labs/skills/tree/main/skills/game-engines/roblox/scenario-roblox-assets) | Use when bringing 3D assets into Roblox Studio or preparing avatar items: import from Blender, GLB, FBX or OBJ files, AI-generated or image-to-3D meshes (Sce… | 1,134 | MIT |
| [roblox-dev-skill](https://github.com/MSayib/roblox-dev-skill) | 让 AI 编程助手成为 Roblox 专家：Luau、引擎 API、架构、反作弊，以及安全驱动 Studio 内置 MCP | 59 | MIT |
| [roblox-ai-skills（合集）](https://github.com/SyphoDev-yt/roblox-ai-skills) | Free Claude Code skills for making Roblox games with AI: code, UI, maps, 3D models (Hi3DGen), animation in Blender, VFX, SFX, textures; build orchestrator. | 54 | NOASSERTION |
| [roblox-vfx-animation（vfxskill）](https://github.com/adnvli/vfxskill) | Claude skill for polished Roblox VFX animations via Roblox Studio MCP — particles, beams, trails, slashes, spells, auras, camera shake. | 30 | MIT |
| [roblox-avatar-creator](https://github.com/poorvith-mp/skills-gamedev/tree/main/skills/roblox-avatar-creator) | Moved to modernized catalog in skillary. | 5 | MIT |
| [roblox-dev-kit](https://github.com/WojciechJelen/roblox-dev-kit) | Roblox 开发套件：Claude Code 插件 + Agent Skills（Rojo 工具链、严格 Luau 模板、Roblox Studio 和 Blender MCP） | 0 | MIT |
| [roblox-luau-skill](https://github.com/2328312928-commits/roblox-luau-skill) | Roblox/Luau 的模拟器与大亨类经济设计 skill，带节奏计算器（成本曲线、重生、离线收益、概率披露） | 0 | MIT |

## 其他引擎与 Web / Other Engines & Web

| 名称 | 说明 | ★ | 许可证 |
|---|---|---|---|
| [love2d-core](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/other-engines/love2d-core) | Structure and debug a LÖVE (Love2D) game in Lua: the love.load/update/draw loop, delta-time movement, input, and screen states. | 4,334 | Apache-2.0 |
| [pygame-core](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/other-engines/pygame-core) | Structure a pygame (pygame-ce) game in Python: the init/event/update/draw loop, delta-time movement, Surface/Rect blitting, keyboard/mouse input, and Sprite/… | 4,334 | Apache-2.0 |
| [threejs-game-skills（合集）](https://github.com/majidmanzarpour/threejs-game-skills) | Agent skills for building playable, polished Three.js browser games: gameplay, AAA-style graphics, UI, QA, optional AI-generated 3D/image/audio assets (9 ski… | 2,587 | MIT |
| [ns-game-apple-arm-port](https://github.com/realskyrin/ns-game-apple-arm-port) | 将 Nintendo Switch 游戏原生适配到 Apple Silicon macOS/iPadOS/iOS（Rust 兼容层 + Metal），含版本识别、ARM64 离线改写、NVN→Metal、实机验收。 | 506 | MIT |
| [glade-mcp](https://github.com/Glade-tool/glade-mcp) | 把任意 MCP 客户端接到 Unity 或 Godot：275+ 细粒度工具、编辑器感知提示词、GDD 项目上下文、脚本语义搜索 | 212 | MIT |
| [Summer Engine skills](https://github.com/SummerEngine/summer) | 为 AI 设计的游戏引擎：MCP、CLI 和 skills，让 agent 构建、测试、发布完整游戏 | 88 | MIT |
| [ludra](https://github.com/ersingvn/ludra) | 为 AI agent 设计的 2D 游戏引擎：游戏是 JSON 场景，ludra check 报错附修复建议，headless 自测打分，带 Claude Code 插件和 skill | 16 | MIT |
| [pyxel-skill](https://github.com/kitao/pyxel-skill) | Claude Code skill for retro game development with Pyxel (by Pyxel's author kitao). | 15 | MIT |
| [port2browser](https://github.com/infinuts/port2browser) | 帮编程 agent 把离线游戏移植到现代浏览器运行（10-16 新建） | 10 | MIT |
| [CometWorks/skills（Space Engineers，合集）](https://github.com/CometWorks/skills) | Skill library for Space Engineers plugin, mod and in-game script development. | 10 | MIT |
| [CitiesSkylines agents-plugins](https://github.com/CitiesSkylinesModding/agents-plugins) | Claude/Codex plugin with MCP server and skills to drive Coherent Gameface game UI | 7 | MIT |
| [gamecraft](https://github.com/taktekhq/gamecraft) | 做 CrazyGames / Poki 休闲网页游戏的 agent skills：设计、画面、资产、上线 | 0 | MIT |

## 美术资产与角色 / Art Assets & Characters

| 名称 | 说明 | ★ | 许可证 |
|---|---|---|---|
| [art-bible](https://github.com/Donchitos/Claude-Code-Game-Studios/tree/main/.claude/skills/art-bible) | Author the Art Bible — visual identity gating asset production. | 27,558 | MIT |
| [img2threejs](https://github.com/img2threejs/img2threejs) | Rebuild the object in a reference image as a code-only, procedural, quality-gated, animation-ready Three.js model (token-efficient image-to-3D skill/plugin). | 19,257 | Apache-2.0 |
| [image-blaster（合集）](https://github.com/neilsonnn/image-blaster) | An image-to-world skillset for Claude: one image to 3D objects (.glb/.obj), explorable 3D scene (.spz) and SFX; usable in Unity/Unreal/Godot/Blender/Three.js… | 12,078 | MIT |
| [image-blast-3d](https://github.com/neilsonnn/image-blaster/tree/main/.claude/skills/image-blast-3d) | Generate one specified atomic 3D object. | 12,078 | MIT |
| [image-blast-image-edit](https://github.com/neilsonnn/image-blaster/tree/main/.claude/skills/image-blast-image-edit) | Generate one image edit from explicit input images and a prompt. | 12,078 | MIT |
| [image-blast-plate](https://github.com/neilsonnn/image-blaster/tree/main/.claude/skills/image-blast-plate) | Generate one clean plate/source cleanup image for an IMAGE-BLASTER world. | 12,078 | MIT |
| [image-blast-project](https://github.com/neilsonnn/image-blaster/tree/main/.claude/skills/image-blast-project) | Create, inspect, and manage an IMAGE-BLAST project envelope under worlds/<slug>. | 12,078 | MIT |
| [image-blast-sfx](https://github.com/neilsonnn/image-blaster/tree/main/.claude/skills/image-blast-sfx) | Generate and post-process a clean sound effect, object impact, or ambient loop. | 12,078 | MIT |
| [image-blast-uncover](https://github.com/neilsonnn/image-blaster/tree/main/.claude/skills/image-blast-uncover) | Main image analysis skill, object generation, plate decisionmaking, and initial scene description. | 12,078 | MIT |
| [image-blast-wildcard](https://github.com/neilsonnn/image-blaster/tree/main/.claude/skills/image-blast-wildcard) | Discover and run any FAL API model or operation the user requests. | 12,078 | MIT |
| [image-blast-world](https://github.com/neilsonnn/image-blaster/tree/main/.claude/skills/image-blast-world) | Generate the 3D static environment of a world from a source or plate image. | 12,078 | MIT |
| [fal-assets](https://github.com/rehan-remade/universal-modder/tree/main/.agents/skills/fal-assets) | Generate game assets with fal (fal.ai) through the fal MCP server, the `um fal` CLI (REST) or `fal api`. | 8,962 | MIT |
| [asset-pipeline](https://github.com/rehan-remade/universal-modder/tree/main/.agents/skills/asset-pipeline) | Turn generated or hand-made art into exactly what a game engine loads. | 8,962 | MIT |
| [create-game-assets](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/disciplines/create-game-assets) | Plan, generate, source, normalize, and validate cohesive visual game assets. | 4,334 | Apache-2.0 |
| [shader-programming](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/disciplines/shader-programming) | Write game shaders from cross-engine fundamentals — the vertex→fragment pipeline, coordinate spaces, UV math, and common 2D/3D effects (tint, UV scroll, diss… | 4,334 | Apache-2.0 |
| [dsh-blender-plugin](https://github.com/sixtysevenlf/dsh-blender-plugin) | DSH（DeepSeek Harness）× Blender 实时插件：15 个模型工具让 AI 驱动 GUI Blender，随包建模 skill。 | 1,291 | BSD-3-Clause |
| [scenario-blender-hard-surface](https://github.com/scenario-labs/skills/tree/main/skills/dcc/blender/scenario-blender-hard-surface) | Use when modeling hard-surface objects in Blender (sci-fi panels, props, weapons, vehicles, robots, machined or product parts) with booleans and cutters, bev… | 1,134 | MIT |
| [scenario-blender-rigging](https://github.com/scenario-labs/skills/tree/main/skills/dcc/blender/scenario-blender-rigging) | Use when rigging a character, creature or prop in Blender through Python: "rig this character", Rigify metarig fitting or generation errors, automatic weight… | 1,134 | MIT |
| [AssetFurnace（image-to-3dlab）](https://github.com/Bingeljell/image-to-3dlab) | Open-source image-to-3D pipeline: prompt or picture to textured, rigged, animated game character, locally; v0.5.0 improves faces | 972 | Apache-2.0 |
| [game-art-direction](https://github.com/zenstory-ai/novel-to-game/tree/main/skills/game-art-direction) | Direct game art and creative vision. | 924 | MIT |
| [game-concept](https://github.com/zenstory-ai/novel-to-game/tree/main/skills/game-concept) | Design game concepts from a novel. | 924 | MIT |
| [3dviz-pro-max](https://github.com/viettranx/3dviz-pro-max/tree/main/skills/3dviz-pro-max) | Design and build expressive 3D scenes, explainers and interactive models with grounded subject knowledge. | 902 | MIT |
| [Scenario for Blender（blender-plugin）](https://github.com/scenario-labs/blender-plugin) | Scenario for Blender: AI images, video, 3D and PBR materials in the viewport, plus a local MCP server for agents (greybox from text, scene captures as input). | 839 | GPL-3.0 |
| [blender-addon-development](https://github.com/EL4CTEO/blender-skills/tree/main/skills/blender-addon-development) | Write Blender 5.2 add-ons as extensions - blender_manifest.toml, operators/panels/menus/property groups/preferences, bpy.props rules after 5.0, undo/redo, mo… | 507 | MIT |
| [blender-animation](https://github.com/EL4CTEO/blender-skills/tree/main/skills/blender-animation) | Animation in Blender 5.2 - slotted/layered actions and the channelbag API, Python keyframing, F-curves, game loops, NLA clips, pose library, mocap/BVH retarg… | 507 | MIT |
| [blender-asset-qa](https://github.com/EL4CTEO/blender-skills/tree/main/skills/blender-asset-qa) | Mandatory review gate for any mesh or asset created or edited in Blender. | 507 | MIT |
| [blender-character-rigging](https://github.com/EL4CTEO/blender-skills/tree/main/skills/blender-character-rigging) | Character rigging in Blender 5.2 - Rigify metarig fit/generate, bone naming/roll/collections, DEF/MCH/control layers, IK/FK, robust skinning (heat + proxy fa… | 507 | MIT |
| [blender-core](https://github.com/EL4CTEO/blender-skills/tree/main/skills/blender-core) | Foundation for any Blender 5.2+ task an agent drives - running bpy via MCP (live) or headless CLI, context overrides, locale-safe node lookup, enum discovery… | 507 | MIT |
| [blender-export-pipelines](https://github.com/EL4CTEO/blender-skills/tree/main/skills/blender-export-pipelines) | Export from Blender 5.2 with verified presets - Roblox (FBX/glTF, cages, R15, SurfaceAppearance), Unity (FBX, Humanoid), Unreal (FBX skeletal, Nanite, UCX), … | 507 | MIT |
| [blender-facial-shapekeys](https://github.com/EL4CTEO/blender-skills/tree/main/skills/blender-facial-shapekeys) | Facial rigs and shape keys in Blender 5.2 - ARKit 52 blendshapes, visemes for lip-sync, sculpting expressions, splitting symmetric shapes into Left/Right, mi… | 507 | MIT |
| [blender-game-optimization](https://github.com/EL4CTEO/blender-skills/tree/main/skills/blender-game-optimization) | Optimize Blender assets for real-time engines - triangle/material/texture/bone budgets per platform (mobile, Roblox, web, VR, console, PC), LOD chains, decim… | 507 | MIT |
| [animate](https://github.com/with-pebbly/aseprite-ai-artist/tree/main/skills/animate) | Build an idle, walk, run or attack cycle from key poses, set timing that reads as motion rather than a metronome, tag it, and review it as a filmstrip. | 476 | MIT |
| [concept](https://github.com/with-pebbly/aseprite-ai-artist/tree/main/skills/concept) | Before drawing a new character, prop, scene or animation, write an art spec, turn it into a ready-to-paste prompt for an image-generation model, and offer th… | 476 | MIT |
| [draw](https://github.com/with-pebbly/aseprite-ai-artist/tree/main/skills/draw) | Draw a sprite from silhouette to finished pixels, in the order that catches mistakes while they are still cheap — block in, check the silhouette, shade, outl… | 476 | MIT |
| [claude-pxl](https://github.com/crsolver/claude-pxl) | Claude skill: generate animated pixel art in code (multi-layer parallax, depth/perspective, edit existing assets), no image model needed | 446 | MIT |
| [mixamo-llm-mocap](https://github.com/squall01337/mixamo-llm-mocap) | Turn any video into a Mixamo-rig animation (GVHMR estimator, spec-driven retarget, FK apply in Blender via MCP); built to be operated end-to-end by an AI agent. | 406 | NOASSERTION |
| [vocaloid-style-mv](https://github.com/EGSECDA/vocaloid-style-mv-pipeline/tree/main/skills/vocaloid-style-mv) | Vocaloid 风手绘歌词 MV 生产管线和 Claude Code skill：Canvas2D/WebGL2 动画引擎、歌词动效、AI 插画、Blender 卡通渲染 3D | 216 | MIT |
| [effekseer-vfx-skill](https://github.com/kanaworksai-hue/effekseer-vfx-skill) | Author real-time game VFX as code for Effekseer and verify them in real Godot renders; plus a vfx-review rubric skill. | 53 | MIT |
| [procedural-blender-nodes（video-to-blender）](https://github.com/gokayfem/video-to-blender/tree/main/skills/procedural-blender-nodes) | Builds, debugs, and art-directs procedural Blender node systems from Python: Geometry Nodes generators and modifiers, Shader Node materials, simulation and r… | 53 | MIT |
| [SpriteCook skills](https://github.com/SpriteCook/skills) | Skills for autonomous agents generating pixel art using SpriteCook | 48 | MIT |
| [Rigby2D](https://github.com/jaisurya-dev-art/rigby2d) | Open-source 2D skeletal animation editor (rig PSD/PNG, animate, export JSON/.skel + atlas; runtimes for JS, Rust, Godot 4) with a built-in MCP server so AI a… | 45 | Apache-2.0 |
| [blender-asset-studio](https://github.com/new-experement/blender-asset-studio) | Semi-autonomous 3D asset creation in Blender via Blender MCP with Codex/Claude Code: reference intake, blockout→pilot→finish, visual self-review, verified ex… | 44 | MIT |
| [3d-asset-pipeline](https://github.com/DECRUX9812/hermes-plugin-gameforge/tree/main/skills/3d-asset-pipeline) | Generate, preview and animate 3D game models as glTF. | 41 | MIT |
| [blender-pipeline](https://github.com/DECRUX9812/hermes-plugin-gameforge/tree/main/skills/blender-pipeline) | Convert, LOD, render and animate models in headless Blender. | 41 | MIT |
| [pixel-art-pipeline](https://github.com/DECRUX9812/hermes-plugin-gameforge/tree/main/skills/pixel-art-pipeline) | Make sprite sheets, tilesets and icons for 2D games. | 41 | MIT |
| [game-asset-aesthetic-test（合集）](https://github.com/zeroa234/game-asset-aesthetic-test) | 8 个游戏美术 Agent Skills：像素精灵（视频转循环精灵）、Spine 骨骼动画（切件/正侧背多视图/立绘）、方块角色（Blockbench/YSM）与讲解配音。 | 32 | 无 |
| [game-asset-spine-multiview](https://github.com/zeroa234/game-asset-aesthetic-test/tree/main/extensions/skills/game-asset-spine-multiview) | 制作正面、侧面和背面多套 Spine 角色，并在 three.js 场景按镜头夹角切换，适用于饥荒式二维角色与三维场景结合的游戏。 | 32 | 无 |
| [game-asset-video-sprites](https://github.com/zeroa234/game-asset-aesthetic-test/tree/main/extensions/skills/game-asset-video-sprites) | 将角色参考图和动作视频制作成循环像素精灵，处理首尾衔接、高清色键、共享裁切和全局调色板。适用于视频帧路线，不负责骨骼绑定。 | 32 | 无 |
| [game-asset-blocky-character](https://github.com/zeroa234/game-asset-aesthetic-test/tree/main/extensions/skills/game-asset-blocky-character) | 用旋转方块和像素贴图制作普通着装的 Minecraft/YSM 风格角色，按社区样本选比例、组织衣身和逐面 UV，并区分 Generic 与目标游戏格式。 | 32 | 无 |
| [aseprite-automation (spa)](https://github.com/aigengame/aseprite-automation/tree/main/skills/spa) | 用 AI agent 自动操作 Aseprite：创建、编辑、校验和导出像素画与 sprite 动画，提供 CLI、Agent Skill 和 MCP 三种接入 | 25 | MIT |
| [vex](https://github.com/uilianks/vex) | 2D vector game art as code: DSL exporting SVG/PNG sprites, animations and atlases with a live viewer (inspired by claude-pxl) | 23 | MIT |
| [Wuxin-Film-Skill（合集）](https://github.com/Yunwuxin-666/Wuxin-Film-Skill) | Unified film, animation, game-art, character, environment, VFX, camera, lighting, style and AI-video prompt production suite (character-design, environment-c… | 19 | — |
| [video-to-3d](https://github.com/enwong93-sketch/video-to-3d) | Turn a single-character A-pose orbit video or an approved whole multi-view character sheet into an editable Blender model using local MiniMax H3 MAIN/H3 IR g… | 12 | MIT |
| [animate-character（claude-skill-klingai-animation）](https://github.com/TamerinTECH/claude-skill-klingai-animation) | Generate character animations from a source image using Kling AI video generation (direct API or via the Higgsfield CLI), then convert the resulting MP4 vide… | 11 | MIT |
| [ai-skills-blender（合集）](https://github.com/SamuelAsherRivello/ai-skills-blender) | Blender skills for Codex and Claude Code powered by Blender Lab MCP: 2D-to-3D, 3D-to-sprite sheets, environments, greybox, models, rig/animate, game export | 9 | MIT |
| [blender-convert-3d-2d](https://github.com/SamuelAsherRivello/ai-skills-blender/tree/main/.claude/skills/blender-convert-3d-2d) | Convert Blender models into consistent 2D views, sprites or sprite sheets using fixed cameras and frame metadata. | 9 | MIT |
| [blender-rig-animate](https://github.com/SamuelAsherRivello/ai-skills-blender/tree/main/.claude/skills/blender-rig-animate) | Rig Blender assets and create named animation clips with deformation and motion checks. | 9 | MIT |
| [blender-game-export](https://github.com/SamuelAsherRivello/ai-skills-blender/tree/main/.claude/skills/blender-game-export) | Export Blender assets for a specified game engine with scale, pivot, material and animation checks. | 9 | MIT |
| [blender-convert-2d-3d](https://github.com/SamuelAsherRivello/ai-skills-blender/tree/main/.claude/skills/blender-convert-2d-3d) | Reconstruct a Blender relief or full model from supplied imagery with explicit depth and hidden-surface assumptions. | 9 | MIT |
| [aseprite-live](https://github.com/N7z/aseprite-live) | Watch an AI agent draw pixel art in Aseprite, live, in your browser | 8 | AGPL-3.0 |
| [hybrid-creature-modeling](https://github.com/phumrapee47/hybrid-creature-modeling) | Claude Code skill：在 Blender 里用混合管线（放样、体素融合、脚本雕刻、烘焙游戏网格）建 3D 生物模型，附 5 种方法对比基准 | 1 | 未声明 |
| [Puppet（木偶人）](https://github.com/Damengxin-123/Puppet) | 基于 Godot 和 C++ 的角色骨骼动画制作工具，含 MCP 服务、现成动画和角色绑定数据 | 1 | 未声明 |
| [aseprite-lua-mcp](https://github.com/alpsei/aseprite-lua-mcp) | 通过 Lua 脚本驱动 Aseprite CLI 的 MCP 服务，v0.2.0 支持内联图片预览、编辑已有 sprite、精简 Lua API 文档 | 1 | MIT |
| [stable-sprite-animation](https://github.com/charolettebradford1361985svo-bit/stable-sprite-animation) | 保持参考图不走样的 sprite 动画 skill：四肢完整的走路、小跳，输出透明 PNG 序列和 GIF | 0 | MIT |
| [aimation](https://github.com/rathouse2002-web/aimation) | 游戏角色动画 skill 合集，含用 MiniMax H3 生成八方向 sprite 动作 | 0 | 未声明 |
| [spriteloom-mcp](https://github.com/AlexPascu007/spriteloom-mcp) | SpriteLoom MLX 的本地像素画 MCP 工具和 agent skill（基于 vkarach/spriteloom，Apple Silicon 本地跑） | 0 | Apache-2.0 |
| [rng-vfx](https://github.com/MRRengi/rng-vfx) | 游戏特效 agent skill：动漫、卡通、风格化、暗黑奇幻、像素、写实等风格，支持 Unity VFX Graph、Unreal Niagara、three.js | 0 | MIT |
| [animated-pixel-art-studio](https://github.com/hrusyd/animated-pixel-art-studio) | 做清晰像素动画、循环 GIF 和 MP4 的 agent skill，带可编辑场景和渲染器 | 0 | MIT |
| [pixelwright](https://github.com/m4bwav/pixelwright) | 用代码画并动画化像素画的 agent 工具：网格对齐、调色板锁定、tile、遮罩动画、sprite sheet，带校验关卡 | 0 | MIT |
| [blender-godot-lowpoly](https://github.com/goordonbear/blender-godot-lowpoly) | Blender 无头程序化建模 + Godot 4 低多边形管线（放样、卡通着色、像素描边、跑酷架构） | 0 | MIT |
| [godot-sprite-mcp](https://github.com/huha007/godot-sprite-mcp) | Godot 4 轻量 MCP 和 CLI：自动切 2D sprite sheet、导出 SpriteFrames、生成脚底对齐碰撞体 | 0 | MIT |
| [game-asset-skills](https://github.com/crapthings/game-asset-skills) | Codex 游戏资产 skills：资产分析、图像生成、透明底资产处理 | 0 | 未声明 |

## 美术风格与像素 / Art Styles & Pixel Art

| 名称 | 说明 | ★ | 许可证 |
|---|---|---|---|
| [diorama（Sloemo）](https://github.com/sloemo01/diorama) | 像素风等距微缩场景（diorama）的 agent skill：先调研再搭建，锁定机位、调色板吸附、有序抖动、描边，自带会动的小人物，用 Three.js 输出 | 45 | MIT |
| [Starry-Night（像素动画 skill）](https://github.com/Khalidabdi1/Starry-Night) | 以梵高《星夜》为蓝本的像素动画组件 agent skill：旋转星空、摇摆柏树、亮灯村庄、随风散开的文字 | 4 | MIT |
| [diorama（educlopez）](https://github.com/educlopez/diorama) | 一组生成会动的等距插画的 agent skills，每个是独立 HTML：SVG 人物 6 种主题，Three.js 微缩世界 4 种质感 | 3 | MIT |

## 音效 / Audio

| 名称 | 说明 | ★ | 许可证 |
|---|---|---|---|
| [team-audio](https://github.com/Donchitos/Claude-Code-Game-Studios/tree/main/.claude/skills/team-audio) | Orchestrate the audio team — audio-director, sound-designer, technical-artist, gameplay-programmer — direction through implementation. | 27,558 | MIT |
| [audio-design](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/disciplines/audio-design) | Implement game audio practice — bus/mixer architecture and gain in decibels, ducking (sidechain), adaptive/dynamic music via layering and re-sequencing, SFX … | 4,334 | Apache-2.0 |
| [NPCTalk（合集）](https://github.com/christos-antono/NPCTalk) | Make any NPC in any game talk back with Fish Audio: skills, a self-hosted voice server and tools for AI coding agents (voice cloning, NPC dialogue/actions, s… | 209 | MIT |
| [game-audio](https://github.com/DECRUX9812/hermes-plugin-gameforge/tree/main/skills/game-audio) | Design game sound effects, music loops and NPC voices. | 41 | MIT |
| [BabelDub](https://github.com/KROU4/BabelDub) | 把游戏翻译并用原角色声音重新配音的 agent：Agent Skills + Claude Code 插件 + 本地模型 CLI（VoxCPM2 + RVC，支持 FMOD/Unity/Wwise） | 0 | MIT |

## 测试、逆向与发布 / Testing, RE & Release

| 名称 | 说明 | ★ | 许可证 |
|---|---|---|---|
| [playtest-report](https://github.com/Donchitos/Claude-Code-Game-Studios/tree/main/.claude/skills/playtest-report) | Structured playtest report template, or turn existing playtest notes into structured feedback. | 27,558 | MIT |
| [performance-optimization](https://github.com/gamedev-skills/awesome-gamedev-agent-skills/tree/main/skills/disciplines/performance-optimization) | Find and fix game performance problems methodically — measure with the engine profiler first, reason about the frame-time budget, locate the CPU-vs-GPU bottl… | 4,334 | Apache-2.0 |
| [game-build](https://github.com/zenstory-ai/novel-to-game/tree/main/skills/game-build) | Build a risk-matched whitebox or the approved production game for its target runtime. | 924 | MIT |
| [game-qa](https://github.com/zenstory-ai/novel-to-game/tree/main/skills/game-qa) | Verify a game with evidence on its selected target runtime. | 924 | MIT |
| [export](https://github.com/with-pebbly/aseprite-ai-artist/tree/main/skills/export) | Produce the files an engine actually consumes — spritesheets with atlases, GIFs, scaled PNGs — with the tags and layout the target needs. | 476 | MIT |
| [editing-gameplay-montages](https://github.com/gustavomenani/editing-gameplay-montages) | Edit gameplay clips (Valorant, CS2, Fortnite) into a music-synced highlight montage / TikTok edit with beat sync, slow motion (RIFE), speed ramps. | 73 | NOASSERTION |
| [game-client-to-server-reverse](https://github.com/ShrugYu/game-client-to-server-reverse) | 从游戏客户端反推服务端协议并复现可部署服务端（Unity/UE/Cocos，IL2CPP/Lua/JS） | 46 | AGPL-3.0 |
| [playtesting](https://github.com/DECRUX9812/hermes-plugin-gameforge/tree/main/skills/playtesting) | Playtest builds and turn reports into fixes. | 41 | MIT |
| [ship-it](https://github.com/DECRUX9812/hermes-plugin-gameforge/tree/main/skills/ship-it) | Export games to the web, phones, itch.io and desktop. | 41 | MIT |
| [playtesting](https://github.com/poorvith-mp/skills-gamedev/tree/main/skills/playtesting) | Structure playtest sessions and sort responses into UX friction, difficulty calibration and feature signal. | 5 | MIT |
| [underhood-skill](https://github.com/Bambeek/underhood-skill) | 给自己拥有的游戏和应用做 mod 的 Claude skills：侦察、逆向、构建并在游戏内验证、本地资产、发布，不用付费 API | 0 | 未声明（NOASSERTION） |

## 贡献指南 / Contributing

欢迎提 PR 或 Issue 补充条目：

1. 条目必须和 AI Agent 做游戏直接相关（Skill、MCP、插件、工具或工作流）。
2. 在对应分类表格里加一行：`[名称](链接) | 一句话说明 | 星数 | 许可证`，同时更新 `data/skills.json`。
3. 链接必须可访问；已归档、404 或纯推广的条目会被移除。
4. 一个 PR 尽量只做一类改动。

## 许可证 / License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

本列表以 CC0 1.0 发布。各条目项目遵循其各自的许可证。
