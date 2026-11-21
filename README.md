Roblox Studio Mobile Source Code

An experimental Android-based 3D studio engine, runtime environment, and script editor inspired by Roblox Studio.

Overview

This repository contains the complete source code archive for the com.exampletest.mobilestudiotest package. The codebase implements an end-to-end mobile development environment capable of rendering 3D scenes, executing Luau scripts, parsing proprietary binary and XML formats, and providing a desktop-class Studio interface optimized for touch displays.

Source Archive Contents

The complete source code is bundled inside mobile studio src.zip, comprising 178 source files organized under the primary package structure:

com/exampletest/mobilestudiotest/
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

Credits to his owner (who dropped his apk, thanks for helping mobile users to make this posible with claude🤣🤣, this project can be prompted in minutes-hours😭): https://www.youtube.com/@fiowwwys
Setup & Compilation

Prerequisites

IDE: Android Studio (Ladybug / Jellyfish or newer)

Java Development Kit: JDK 17+

Android SDK: Target API 34+ / Minimum API 24 (Android 7.0)

Step-by-Step Instructions

Clone the repository:

git clone https://github.com/Helloneighbor-crypto/RobloxStudioMobileSourceCode.git

Open the project in Android Studio and synchronize Gradle files.

Build the debug binary:
./gradlew assembleDebug



Disclaimer: This project is provided for educational, reverse-engineering, and research purposes. All trademarks, protocols, and data structures related to Roblox remain the property of their respective owners.
