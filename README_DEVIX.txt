============================================================
Manual Transmission v5.6.1 [rework by DeViX]
Compatible with GTA V 1.0.3095.0 - 1.0.3889.0+
============================================================

Changelog & Fixes by DeViX:
1. Fixed Crash on Vehicle Entry:
   - Resolved NULL pointer dereference in GetAddressOfEntity.
   - Integrated dynamic ScriptHookV entity address hook into Gears.asi.
   - Prevents Script Hook V Error (Exception addr 0x0000000000000000).

2. Fixed Steering Wheel Controls for Cars:
   - Patched WheelInput steering pipeline in Gears.asi.
   - Re-routed steering wheel angle directly to game ControlVehicleMoveLeftRight.
   - Fully restores steering wheel turning for all vehicles without Patreon paywall.

3. In-Game Menu:
   - Press '[' (or Russian 'Х') to open the configuration menu.
   - Cheat code: mtmenu

Installation:
   - Copy 'Gears.asi' and the 'ManualTransmission' folder into your GTA V directory.
   - Requires ScriptHookV and dinput8.dll.
============================================================
