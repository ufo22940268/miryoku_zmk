# Temper Build Commands

## Build & Flash Left (central, connects to computer via BLE)

```bash
source ~/IdeaProjects/zmk/.venv/bin/activate.fish; and cd ~/IdeaProjects/zmk/app; and west build -p -d build/temper_left -b nice_nano_v2 -- -DSHIELD="temper_left" -DZMK_CONFIG="$HOME/IdeaProjects/miryoku_zmk/config"; and west flash -d build/temper_left
```

## Build & Flash Right (peripheral)

```bash
source ~/IdeaProjects/zmk/.venv/bin/activate.fish; and cd ~/IdeaProjects/zmk/app; and west build -p -d build/temper_right -b nice_nano_v2 -- -DSHIELD="temper_right" -DZMK_CONFIG="$HOME/IdeaProjects/miryoku_zmk/config"; and west flash -d build/temper_right
```

## Reset BLE Bonds (run before first use)

```bash
source ~/IdeaProjects/zmk/.venv/bin/activate.fish; and cd ~/IdeaProjects/zmk/app; and west build -p -d build/settings_reset -b nice_nano_v2 -- -DSHIELD="settings_reset"; and west flash -d build/settings_reset
```
