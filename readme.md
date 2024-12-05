# Quick guide for setting up the firmware

```sh
    qmk json2c <keymap>.json -o <keymap>.c
    qmk compile -kb kinesis/<firmware> -km <keymap>
```

# Example with this specific configuration

First convert the `keymap.json` into a `keymap.c` if any changes were done, from an outside tool to the `keymap.json` file, move any
relevant code from the original `keymap.c` back into the new `keymap.c` generated from the `keymap.json,` by `json2c`. Note that the
current `keymap.json` is actually named `_keymap.json` to avid `qmk` picking it up over the `keymap.c` file

```sh
    qmk json2c keyboards/kinesis/keymaps/kinesismod/_keymap.json > keymap.c
    qmk compile -kb kinesis/nguyenvietyen -km kinesismod
```

`If a keymap.json is present and a keymap.c, the keymap.json will win over, and will be the one picked up by the qmk compiler`
