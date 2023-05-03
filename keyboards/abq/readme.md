# ABQ

* Hardware Availability: https://sonatina.jp

Make example for this keyboard (after setting up your build environment):

    qmk compile -kb abq -km default

Flashing example for this keyboard:

    qmk flash -kb abq -km default

See the [build environment setup](https://docs.qmk.fm/#/getting_started_build_tools) and the [make instructions](https://docs.qmk.fm/#/getting_started_make_guide) for more information. Brand new to QMK? Start with our [Complete Newbs Guide](https://docs.qmk.fm/#/newbs).

## Bootloader

Enter the bootloader in 3 ways:

* **Bootmagic reset**: Hold down the key at (0,0) in the matrix (usually the top left key or Escape) and plug in the keyboard
* **Physical reset button**: Briefly press the button on the back of the PCB - some may have pads you must short instead
* **Keycode in layout**: Press the key mapped to `QK_BOOT` if it is available

## Test
* e0a09ff728 2023-04-17 GMMK 2 volume up/down Fn keys are backwards in default mapping (#20476)
```sh
qmk compile -kb abq -km default
qmk compile -kb abq -km via
qmk compile -kb abq -km nohzen
```

