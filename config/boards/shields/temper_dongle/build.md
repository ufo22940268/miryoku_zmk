# Temper Dongle Build Commands

## Build & Flash Dongle (central, USB to computer)

```bash
source ~/IdeaProjects/zmk/.venv/bin/activate.fish; and cd ~/IdeaProjects/zmk/app; and west build -p -d build/temper_dongle_dongle -b nice_nano_v2 -- -DSHIELD="temper_dongle_dongle" -DZMK_CONFIG="$HOME/IdeaProjects/miryoku_zmk/config"; and west flash -d build/temper_dongle_dongle
```

## Build & Flash Left (peripheral)

```bash
source ~/IdeaProjects/zmk/.venv/bin/activate.fish; and cd ~/IdeaProjects/zmk/app; and west build -p -d build/temper_dongle_left -b nice_nano_v2 -- -DSHIELD="temper_dongle_left" -DZMK_CONFIG="$HOME/IdeaProjects/miryoku_zmk/config"; and west flash -d build/temper_dongle_left
```

## Build & Flash Right (peripheral)

```bash
source ~/IdeaProjects/zmk/.venv/bin/activate.fish; and cd ~/IdeaProjects/zmk/app; and west build -p -d build/temper_dongle_right -b nice_nano_v2 -- -DSHIELD="temper_dongle_right" -DZMK_CONFIG="$HOME/IdeaProjects/miryoku_zmk/config"; and west flash -d build/temper_dongle_right
```

## Reset BLE Bonds (run before first use)

```bash
source ~/IdeaProjects/zmk/.venv/bin/activate.fish; and cd ~/IdeaProjects/zmk/app; and west build -p -d build/settings_reset -b nice_nano_v2 -- -DSHIELD="settings_reset"; and west flash -d build/settings_reset
```
