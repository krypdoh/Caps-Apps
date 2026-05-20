# Caps&Apps

Caps&Apps is an AutoHotkey v2 utility that automatically enables Caps Lock when specific applications are active and restores it when focus changes.

## Features

- Monitors the active window every 250 ms.
- Turns Caps Lock on for configured `.exe` names.
- Turns Caps Lock off when leaving a configured app (if the script enabled it).
- Tray menu tools to add and remove applications.
- Uses `capsandapps.ico` for tray icon and EXE icon.
- Includes an About dialog in the tray menu.

## Files

- `capsandapps.ahk`: Main AutoHotkey v2 script.
- `capsandapps.ini`: Saved configured application list.
- `capsandapps.ico`: Icon used by tray and compiled executable.
- `capsandapps.exe`: Compiled executable output.

## Requirements

- Windows
- AutoHotkey v2

## Run From Script

1. Install AutoHotkey v2.
2. Run `capsandapps.ahk`.
3. Use the tray icon menu:
   - Add from Running Programs
   - Browse for .exe
   - View/Remove Programs

## Build EXE

Use Ahk2Exe with a v2 base and custom icon:

```powershell
& "C:\Program Files\AutoHotkey\Compiler\Ahk2Exe.exe" \
  /in "C:\path\to\capsandapps.ahk" \
  /out "C:\path\to\capsandapps.exe" \
  /icon "C:\path\to\capsandapps.ico" \
  /base "C:\Program Files\AutoHotkey\v2\AutoHotkey64.exe"
```

## Configuration Storage

Configured applications are stored in `capsandapps.ini` under the `Applications` section.

## License

MIT
