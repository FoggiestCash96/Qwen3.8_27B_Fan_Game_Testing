# Toolchain

## Godot

The Godot editor binary is **not committed** (kept out of the repo via `.gitignore`).
It is installed locally at `tools/godot/`.

To (re)install on a fresh machine:

```bat
curl -L -o godot.zip https://github.com/godotengine/godot/releases/download/4.7.2-stable/Godot_v4.7.2-stable_win64.exe.zip
tar -xf godot.zip
mkdir tools\godot
copy Godot_v4.7.2-stable_win64.exe* tools\godot\
```

- `tools/godot/godot.exe` — editor (GUI)
- `tools/godot/godot_console.exe` — console build, used for headless CI / validation

Verify:

```bat
tools\godot\godot_console.exe --version
:: expected: 4.7.2.stable.official...
```

## Blender

Asset pipeline uses the system Blender (`%ProgramFiles%\Blender Foundation\Blender 4.2\blender.exe`)
in `--background --python` mode. See `tools/blender/` (added in T3).
