# 7sKB QMK Configuration

Personal QMK firmware configuration for the 7sKB split keyboard by Salicylic_acid3.

## Setup

This repository is symlinked to the QMK firmware directory:

```bash
# Symlink already created
ln -s ~/src/github.com/yshrkume/7skb-qmk-config ~/qmk_firmware/keyboards/salicylic_acid3/7skb/keymaps/yshrkume
```

## Features

### Layers

- **Layer 0 (_QWERTY)**: Base QWERTY layout
- **Layer 1 (_FN)**: Function keys, media controls, and navigation
- **Layer 2 (_ADJUST)**: RGB controls and system settings

### RGB Lighting

- Layer indicators via first LED color:
  - Blue: Function layer active
  - Purple: Adjust layer active
  - Default: Base layer
- Custom RGB reset function (RGB_RST)
- Effects range: LEDs 1-11

### Configuration

- Tapping term: 180ms
- Debounce: 2ms
- Quick tap term: 0ms

## Building

From the QMK root directory (`~/qmk_firmware`):

```bash
# Compile firmware
qmk compile -kb salicylic_acid3/7skb/rev1 -km yshrkume

# Or using make
make salicylic_acid3/7skb/rev1:yshrkume
```

## Flashing

1. Put keyboard into bootloader mode (press `QK_BOOT` key or reset button)
2. Flash the firmware:

```bash
qmk flash -kb salicylic_acid3/7skb/rev1 -km yshrkume
```

## Files

- `keymap.c`: Keymap definitions and layer logic
- `config.h`: Hardware configuration and timing settings
- `CLAUDE.md`: Development guidelines for AI assistance

## License

GPL v2 (as per QMK requirements)