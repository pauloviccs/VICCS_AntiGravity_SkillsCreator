---
name: modding-hytale
description: Guides the creation of Hytale mods using Java, ECS, and Prefabs. Use when the user asks about Hytale modding, plugins, or scripting.
---

# Modding Hytale

## When to use this skill

- When the user asks to create a Hytale mod or plugin.
- When the user mentions "Hytale", "Prefabs", or "ECS" in the context of game development.
- When the user needs to handle Hytale server events or edit in-game assets.

## Workflow

1. **Environment Setup**:
    - Ensure Java is installed (Hytale is Java-based).
    - Setup a standard Hytale project structure (typically Maven/Gradle).
2. **Prefab Management** (In-Game):
    - Use `/prefab list` to view existing prefabs.
    - Use `/editprefab load <name>` to modify structures.
    - Save changes with `/editprefab save`.
3. **Event Handling** (Java):
    - Identify the event type: `IEvent` (Server/Global) or `EcsEvent` (Entity/Block interaction).
    - Implement an event listener.
    - Register the listener in the main plugin class.
4. **ECS Implementation**:
    - Define Components (Data).
    - Define Systems (Logic).
    - Attach Components to Entities.

## Instructions

### Prefab Commands

- **/prefab**: Manage prefab files.
  - `load`, `save`, `delete`, `list`
- **/editprefab**: Edit physical structures.
  - `new`: Create new world for prefab creation.
  - `load`: Load existing prefab for editing.
  - `select`: Select area (within 200 blocks).
  - `save`: Save current selection.
  - `setbox`: Define bounding box.

### Event System

Hytale uses a split event system. Choose the correct base class:

#### 1. IEvent (Server Lifecycle & Global)

Used for server-wide states, asset loading, and player connection.

- **Examples**: `PlayerConnectEvent`, `AddWorldEvent`, `PluginSetupEvent`, `ShutdownEvent`.

#### 2. EcsEvent (Gameplay & Interactions)

Used for game logic, physics, and entity interactions.

- **Examples**:
  - `BreakBlockEvent`, `PlaceBlockEvent` (Block modification)
  - `DamageBlockEvent`, `DropItemEvent` (Physics/Inventory)
  - `CraftRecipeEvent` (Crafting)
  - `ChatEvent` (Communication)

### ECS (Entity Component System)

- **Entities**: The objects in the world (Players, Mobs, Items).
- **Components**: Data containers attached to entities (e.g., `PositionComponent`, `HealthComponent`).
- **Systems**: Iterate over entities with specific components to apply logic.

## Resources

- [Hytale Modding Docs](https://hytalemodding.dev/en/docs)
- [Event List](https://hytalemodding.dev/en/docs/server/events)
