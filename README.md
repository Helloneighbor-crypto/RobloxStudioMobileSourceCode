# Roblox Studio Mobile Source Code

> An experimental Android-based 3D studio engine, runtime environment, and script editor inspired by Roblox Studio.

---

## Overview

This repository contains the complete source code archive for the `com.exampletest.mobilestudiotest` package. The codebase implements an end-to-end mobile development environment capable of rendering 3D scenes, executing Luau scripts, parsing proprietary binary and XML formats, and providing a studio interface optimized for mobile devices.

---

## Source Archive Contents

The source code is bundled inside `mobile studio src.zip`, comprising **178 source files** organized under the primary package structure:

```text
mobilestudiosrc/mobilestudiotest/
├── MainActivity.java      # Application entry point and lifecycle management
├── StudioApp.java         # Application context and runtime initializations
├── R.java                 # Resource identifier mappings
├── audio/                 # Spatial audio engine and sound playback
├── core/                  # Core studio state, plugin architecture, undo tree
├── engine/                # 3D physics, CSG operations, skeletal animation
├── format/                # RBX binary/XML serialization and LZ4 decompression
├── lua/                   # Luau transpiler, runtime sandbox, API wrappers
├── model/                 # Data model primitives (CFrame, Vector3, Instance, etc.)
├── net/                   # Roblox Open Cloud integration and asset fetchers
├── render/                # OpenGL ES 3D rendering pipeline, batching, Draco meshes
└── ui/                    # Studio mobile UI, viewport manager, code editor
```

---

## Credits

Credits to the original creator who made this project possible (With ai slop + claude, can be prompted in mins-hours):
* **YouTube:** [Fiowwwys Channel](https://www.youtube.com/@fiowwwys)

---

## Core Modules & Architecture

### 1. Rendering Pipeline (`render`)
* **OpenGL ES Engine:** Core rendering managed by `SceneRenderer`, `MeshBuilder`, `StaticBatches`, and `Frustum` culling.
* **Mesh Handling:** Support for `Draco` mesh compression, `UnionMeshes`, and 3D viewport `AdornHandles`.
* **Camera Systems:** Smooth 3D manipulation via `FlyCamera` and `ViewState` controllers.

### 2. Luau Runtime & Execution (`lua`)
* **Execution Sandbox:** Embedded script environment powered by `LuaRuntime`, `LuauTranspiler`, and `LuaSandbox`.
* **API Bindings:** Emulates standard global environments, services (`RobloxServices`), signals/events (`Connection`, `SignalRef`), and property interpolation (`Tween`, `TweenInfoV`).

### 3. Studio User Interface (`ui`)
* **3D Viewport:** Hardware-accelerated canvas (`ViewportView`).
* **Scene Tree & Properties:** Interactive node inspector (`ExplorerPanel`) and property panel (`PropertiesPanel`).
* **Script Editor:** Embedded code editor (`ScriptEditor`) with syntax auto-completion (`Autocomplete`).
* **Layout Management:** Docking layout system (`DockLayout`, `Splitter`) alongside asset drawers (`ToolboxPanel`, `AudioBrowser`).

### 4. Engine & Simulation (`engine`)
* **Runtime Session:** State orchestration via `PlaySession`.
* **CSG Modeling:** Real-time Constructive Solid Geometry operations (`Csg`, `CollisionMeshes`).
* **Avatar System:** Character model compositing (`Avatar`, `ClothingCompositor`) and skeletal animation (`AnimPlayer`).

### 5. Data Serialization & Storage (`format`)
* **File Parsers:** Complete readers and writers for Roblox binary and XML file structures (`RbxBinaryReader`, `RbxXmlReader`, `RbxBinaryWriter`).
* **Decompression:** Custom `Lz4` stream decoder for binary data chunks.

### 6. Networking & Cloud (`net`)
* **Cloud API Integration:** Services for place management, asset fetching, and authentication (`RobloxApi`, `RobloxCloud`, `AssetFetcher`, `Accounts`).

---

## Setup & Compilation

### Prerequisites
* **IDE:** Android Studio (Ladybug / Jellyfish or newer)
* **Java Development Kit:** JDK 17+
* **Android SDK:** Target API 34+ / Minimum API 24 (Android 7.0)

### Step-by-Step Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/Helloneighbor-crypto/RobloxStudioMobileSourceCode.git
   ```

2. Extract `mobile studio src.zip` into your Android project directory:
   ```text
   mobilestudiosrc/mobilestudiotest/
   ```

3. Open the project in Android Studio and synchronize Gradle files.

4. Build the debug binary:
   ```bash
   ./gradlew assembleDebug
   ```

---

## Disclaimer

This project is provided for educational, reverse-engineering, and research purposes. All trademarks, protocols, and data structures related to Roblox remain the property of their respective owners.
