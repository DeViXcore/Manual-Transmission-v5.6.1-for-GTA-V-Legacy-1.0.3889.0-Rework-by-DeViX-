# GTA V Manual Transmission v5.6.1 (Rework by DeViX)

Custom enhanced and repaired build of the iconic **Manual Transmission & Steering Wheel Mod (Gears.asi)** by *ikt* for **Grand Theft Auto V** (tested & verified on **v1.0.3095.0 – v1.0.3889.0+ Legacy / The Chop Shop / Bottom Dollar Bounties**).

---

## 🌟 Key Changes & Improvements

### 1. 🏎️ Complete Automatic Transmission Engine Rework (R-N-D Mode)
* **Real PRND / R-N-D Shifter Architecture**:
  * Clean, seamless 3-position transmission sequence: **`R` (Reverse) ↔ `N` (Neutral) ↔ `D` (Drive)**.
  * Park (`P`) mode removed for a true racing/sequential paddle experience.
  * **Sequential paddle switching**:
    * **Paddle Up (Shift Up)**: `R` -> `N` -> `D`
    * **Paddle Down (Shift Down)**: `D` -> `N` -> `R`
* **True Reverse Gear (`R`)**:
  * Correctly engages engine reverse without locking neutral or throttle.
* **Automatic Forward Shifts in Drive (`D`)**:
  * Dynamic engine bypass: GTA V's native transmission smoothly manages forward gears (`1..6+`) automatically.
* **Blue HUD Transmission Indicator**:
  * Custom HUD displays the active mode: **`R`**, **`N`**, or **`D`**.

### 2. 🕹️ Steering Wheel Direct Turning Fix
* **Instant Steering Response**:
  * Solved the issue in vanilla v5.6.1 on newer GTA V versions where the steering wheel turned visually, but the car wheels failed to rotate/turn.
  * Direct low-latency hardware wheel angle routing straight into the game physics pipeline (`ControlVehicleMoveLeftRight`).

### 3. 🛡️ ScriptHookV Crash Fix (Dynamic Entity Hook)
* **Eliminated `GetAddressOfEntity` Null Pointer Crash**:
  * Completely fixes the known crash on vehicle entry (`Script Hook V Critical Error: Exception addr 0x0000000000000000`).
  * Uses a clean dynamic call resolver via ScriptHookV's export `?getScriptHandleBaseAddress@@YAPEAEH@Z`.

### 4. ⚙️ Unlocked & Untouched Manual Transmission
* **Sequential (`S`) & H-Pattern (`H`)**:
  * 100% original, unmodified logic for clutch, stalling, engine braking, and downshift protection preserved.

### 5. 🎨 UI & Clean Menu
* **Clean English interface** without broken characters or untranslated labels.
* **Bypassed annoying popups** ("Patch test error" / "New update available").
* Header subtitle: `5.6.1 for GTA V Legacy 1.0.3889.0 by DeViX`.

---

## 📁 Repository Structure

```
├── Gears.asi                    # Main patched ASI mod binary
├── README.md                    # Project documentation
├── .gitignore                   # Git ignore file
└── ManualTransmission/          # Configuration directory
    ├── settings_general.ini     # General mod & HUD settings
    ├── settings_wheel.ini       # Steering wheel, pedals & FFB bindings
    ├── settings_controls.ini    # Keyboard & controller bindings
    ├── settings_menu.ini        # In-game menu appearance
    ├── WheelSetup.exe           # Official wheel & FFB configuration tool
    ├── animations.yml           # Shifting animations
    ├── texture_*.png            # Dashboard warning icons (ABS, TCS, ESP, etc.)
    └── Vehicles/                # Custom per-vehicle configurations
```

---

## 🚀 Installation

1. Make sure you have **Script Hook V** (`ScriptHookV.dll`) and an ASI loader (`dinput8.dll`) installed in your main GTA V root folder.
2. Copy `Gears.asi` and the `ManualTransmission` folder into your root GTA V directory:
   ```
   <Path-to-GTA-V>/
   ├── GTA5.exe
   ├── ScriptHookV.dll
   ├── dinput8.dll
   ├── Gears.asi
   └── ManualTransmission/
   ```
3. Launch Grand Theft Auto V.

---

## 🎮 Controls & Menu

* **Open Configuration Menu**: Press `[` (default) or type the cheat `mtmenu`.
* **Configure Steering Wheel & FFB**:
  * Open `ManualTransmission/WheelSetup.exe` while your wheel is connected, or configure directly from the in-game menu under **Wheel Controls**.

---

## 🛠️ Credits & Acknowledgements

* **Original Mod Developer**: [ikt](https://github.com/E6616) for creating Manual Transmission for GTA V.
* **Rework & Fixes**: **DeViX** (ScriptHookV dynamic entity resolution, steering wheel injection, R-N-D automatic controller).