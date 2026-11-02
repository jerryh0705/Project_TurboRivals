# 🏎️ TurboRivals

A fast-paced, **local split-screen (two-player)** arcade racing game built with Unity and C#. Challenge your friends on the same screen using mixed inputs (Keyboard vs. Gamepad), utilize speed boosts, and compete for the fastest lap times on a global leaderboard.

## 🎮 Play the Game
You can play the WebGL build directly in your browser on itch.io:
👉 **[Play TurboRivals on itch.io](https://jhuang02.itch.io/project1-turborivals)**

## ✨ Features
* **Local Split-Screen Multiplayer:** Two players race simultaneously on the same screen.
* **Mixed Input Support:** Seamlessly supports Player 1 on Keyboard and Player 2 on Gamepad simultaneously.
* **Arcade Car Physics:** Responsive and fun vehicle handling.
* **Dynamic Audio:** Engine sound pitch and volume dynamically adjust based on the car's speed.
* **Power-ups:** Collect speed boosts scattered across the track.
* **Lap & Race Tracking:** Real-time lap counting and finish line triggers.
* **Global Leaderboard:** Track your best times and compete with others via the Dreamlo API.
* **Modular UI & Audio:** Persistent audio settings and clean menu transitions.

## 🛠️ Tech Stack & Architecture
* **Engine:** Unity
* **Language:** C#
* **Input System:** Unity Input System (`PlayControl.inputactions` / `GameControl.inputactions`) with `PlayerInputManager` for device assignment.
* **Leaderboard API:** Dreamlo

### Core Systems
* **Controllers:** `CarController.cs` (Handles physics and movement).
* **Camera & View:** Split-screen camera setup using Unity Viewports.
* **Audio:** `CarEngineSound.cs` (Dynamic pitch modulation), `MenuAudioManager.cs`, `AudioSettings.cs`.
* **Race Logic:** `RaceManager.cs`, `RaceStartManager.cs`, `LapCounter.cs`, `FinishLine.cs`.
* **Pickups:** `PowerUpSpawner.cs`, `SpeedBoostPickup.cs`, `PowerUpVisual.cs`.
* **Data & UI:** `RaceHistory.cs`, `DreamloRaceHistory.cs`, `HistoryUI.cs`, `MenuManager.cs`.

## 🚀 How to Run Locally
1. Clone this repository.
2. Open the project in **Unity** (Version `[Insert Unity Version, e.g., 2021.3 LTS]`).
3. Open the `Scenes` folder and load the starting scene.
4. Ensure a **Gamepad is connected** to your PC (for Player 2).
5. Press **Play** in the Unity Editor.

*(Note: The `Library`, `Logs`, and `UserSettings` folders are excluded from this repository via `.gitignore` to keep the repo clean. Unity will regenerate these upon opening the project).*

## 🕹️ Controls
* **Player 1 (Keyboard):** `WASD` or `Arrow Keys` to Drive.
* **Player 2 (Gamepad):** Left Stick / Triggers to Drive.
*(Note: The game requires a connected controller for the local 2-player mode).*

## 👤 Author
**Jerry** - *Solo Developer* 
Designed and programmed all systems including vehicle physics, split-screen implementation, multi-device input handling, UI, audio management, and online leaderboard integration.
