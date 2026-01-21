---
name: modding-hytale
description: Guides the creation of Hytale mods using Java 25 (Server) and Visual Scripting. Covers ECS, Prefabs, Model creation (Blockbench), and V2 World Generation.
---

# Modding Hytale

## When to use this skill

- When the user asks to create a Hytale mod, plugin, or server script.
- When the user mentions "Hytale", "Prefabs", "ECS", "HytaleServer.jar", "Blockbench", or "World Gen V2".
- When creating custom entities, blocks, or modifying world generation logic.

## Workflow

1. **Environment Check & Setup**:
    - **Java 25** (OpenJDK/Adoptium) + **Maven 3.9.12+**.
    - Install `HytaleServer.jar` to local Maven cache (see instructions).
    - Install **Blockbench** + **Hytale Plugin** for asset creation.

2. **Logic Implementation Strategy**:
    - **Performance/Complex Logic**: Use **Java Plugins** (Server-side).
    - **Game Design/Interactions**: Use **Visual Scripting** (Nodes) for accessibility and safe sandboxing.
    - **World Generation**: Use V2 API Code Mods for procedural generation and "Heuristics".

3. **Asset Creation Pipeline**:
    - **Modeling**: Use Cubes and Quads only (No spheres/ngons).
    - **Texturing**: Adhere to density rules (32px/unit for blocks, 64px/unit for characters).
    - **Import**: Use the Hytale Asset Editor to bundle assets.

4. **Event Handling (Java)**:
    - **Lifecycle**: `IEvent` (Boot, Shutdown).
    - **Async**: `IAsyncEvent` (Chat, Data Fetch).
    - **Gameplay**: `EcsEvent` (Block Break, Damage, physics).

## Instructions

### 1. Environment Setup (Critical)

- **Java**: JDK 25 (Adoptium recommended).
- **Maven**: 3.9.12+.
- **HytaleServer.jar**: Must be manually installed.

**PowerShell Install Command:**

```powershell
mvn install:install-file -Dfile="PATH_TO_JAR/HytaleServer.jar" -DgroupId="com.hypixel.hytale" -DartifactId="HytaleServer-parent" -Dversion="1.0-SNAPSHOT" -Dpackaging="jar"
```

### 2. Modeling & Texturing (Blockbench)

Hytale has strict art style guidelines enforced by its renderer.
- **Primitives**: Only Cubes (6 faces) and Quads (2 faces) allowed.
- **Texture Density**:
  - **Props/Blocks**: 32px per unit.
  - **Characters/Items**: 64px per unit (allows more detail for emotional expression).
- **Tools**: Use the **Hytale Blockbench Plugin** to ensure compatibility and correct export formats.

### 3. World Generation V2

The V2 World Gen API allows "Code Mods" to interact with the procedural generator.
- **Heuristics**: Define patterns (e.g., specific tree roots spawning only above caves) to create "readable" environments.
- **Context Awareness**: Use the API to read surrounding blocks/biomes during generation.
- **Thread Safety**: The API is automatically multithreaded; focus on logic, not synchronization.

### 4. Visual Scripting vs. Java

- **Visual Scripting**: The primary tool for *designers*. Use for in-game interactions, quest logic, and simple entity behaviors.
- **Java Plugins**: The tool for *programmers*. Use for new systems, heavy computations, extending the node editor with custom nodes, and server-side infrastructure.

### 5. Event Taxonomy

- **IEvent** (Main Thread): `PluginSetupEvent`, `PlayerConnectEvent`, `AddWorldEvent`.
- **IAsyncEvent** (Threaded): `PlayerChatEvent` (Use for non-blocking comms).
- **EcsEvent** (Gameplay): `BreakBlockEvent`, `DamageBlockEvent`, `CraftRecipeEvent`.

## Resources

- **Official Modding Strategy**: [Hytale Modding Status](https://hytale.com/news/2025/11/hytale-modding-strategy-and-status)
- **World Gen V2**: [Future of World Gen](https://hytale.com/news/2026/1/the-future-of-world-generation)
- **Model Making**: [Making Models for Hytale](https://hytale.com/news/2025/12/an-introduction-to-making-models-for-hytale)
- **Documentation**: [hytalemodding.dev](https://hytalemodding.dev/en/docs)
