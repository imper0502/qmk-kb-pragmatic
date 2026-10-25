# pragmatic

Pragmatic 第二代:5×12 矩陣的分離式鍵盤,使用自訂的 `matrix.c`(`CUSTOM_MATRIX = lite`),bootloader 為 caterina。第一代請見 `pragmatic_classical`。

- Keyboard Maintainer: [James Sa](https://github.com/jamessa)
- Processor: atmega32u4

## Build

在 QMK External Userspace 中編譯(需先設定 `user.overlay_dir`):

    qmk compile -kb pragmatic -km imper0502

See the [QMK build environment setup](https://docs.qmk.fm/#/getting_started_build_tools) for more information.

## Bootloader

Enter the bootloader in 3 ways:

- **Bootmagic reset**: Hold down the key at (0,0) in the matrix (usually the top left key or Escape) and plug in the keyboard
- **Physical reset button**: Briefly press the button on the back of the PCB - some may have pads you must short instead
- **Keycode in layout**: Press the key mapped to `QK_BOOT` if it is available

## Layouts

### LAYOUT_split_4x6_4

```
LAYOUT_split_4x6_4
┌───┬───┬───┬───┬───┬───┐             ┌───┬───┬───┬───┬───┬───┐
│   │   │   │   │   │   │             │   │   │   │   │   │   │
├───┼───┼───┼───┼───┼───┤             ├───┼───┼───┼───┼───┼───┤
│   │   │   │   │   │   │             │   │   │   │   │   │   │
├───┼───┼───┼───┼───┼───┤             ├───┼───┼───┼───┼───┼───┤
│   │   │   │   │   │   │             │   │   │   │   │   │   │
├───┼───┼───┼───┼───┼───┤             ├───┼───┼───┼───┼───┼───┤
│   │   │   │   │   │   │             │   │   │   │   │   │   │
└───┴───┴───┴───┴───┴───┘             └───┴───┴───┴───┴───┴───┘
                ┌───┬───┬───┐     ┌───┬───┬───┐
            ┌───┤   │   │   │     │   │   │   ├───┐
            │   ├───┴───┴───┘     └───┴───┴───┤   │
            └───┘                             └───┘
```

### LAYOUT_split_4x6_3

```
LAYOUT_split_4x6_3
┌───┬───┬───┬───┬───┬───┐             ┌───┬───┬───┬───┬───┬───┐
│   │   │   │   │   │   │             │   │   │   │   │   │   │
├───┼───┼───┼───┼───┼───┤             ├───┼───┼───┼───┼───┼───┤
│   │   │   │   │   │   │             │   │   │   │   │   │   │
├───┼───┼───┼───┼───┼───┤             ├───┼───┼───┼───┼───┼───┤
│   │   │   │   │   │   │             │   │   │   │   │   │   │
├───┼───┼───┼───┼───┼───┤             ├───┼───┼───┼───┼───┼───┤
│   │   │   │   │   │   │             │   │   │   │   │   │   │
└───┴───┴───┴───┴───┴───┘             └───┴───┴───┴───┴───┴───┘
                ┌───┬───┬───┐     ┌───┬───┬───┐
                │   │   │   │     │   │   │   │
                └───┴───┴───┘     └───┴───┴───┘
```

### LAYOUT_split_3x6_3

```
LAYOUT_split_3x6_3
┌───┬───┬───┬───┬───┬───┐             ┌───┬───┬───┬───┬───┬───┐
│   │   │   │   │   │   │             │   │   │   │   │   │   │
├───┼───┼───┼───┼───┼───┤             ├───┼───┼───┼───┼───┼───┤
│   │   │   │   │   │   │             │   │   │   │   │   │   │
├───┼───┼───┼───┼───┼───┤             ├───┼───┼───┼───┼───┼───┤
│   │   │   │   │   │   │             │   │   │   │   │   │   │
└───┴───┴───┴───┴───┴───┘             └───┴───┴───┴───┴───┴───┘
                ┌───┬───┬───┐     ┌───┬───┬───┐
                │   │   │   │     │   │   │   │
                └───┴───┴───┘     └───┴───┴───┘
```

### LAYOUT_split_3x5_2

```
LAYOUT_split_3x5_2
    ┌───┬───┬───┬───┬───┐             ┌───┬───┬───┬───┬───┐
    │   │   │   │   │   │             │   │   │   │   │   │
    ├───┼───┼───┼───┼───┤             ├───┼───┼───┼───┼───┤
    │   │   │   │   │   │             │   │   │   │   │   │
    ├───┼───┼───┼───┼───┤             ├───┼───┼───┼───┼───┤
    │   │   │   │   │   │             │   │   │   │   │   │
    └───┴───┴───┴───┴───┘             └───┴───┴───┴───┴───┘
                    ┌───┬───┐     ┌───┬───┐
                    │   │   │     │   │   │
                    └───┴───┘     └───┴───┘
```

## License

Source files are licensed under GPL-2.0-or-later, see the license header of each file. `matrix.c` is derived from QMK (Jun Wako, Jack Humbert, Yiancar); the keyboard is based on work by James Sa.
