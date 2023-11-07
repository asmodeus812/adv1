# Quick guide for setting up the firmware
 qmk compile -kb kinesis/<firmware> -km <keymap>
 qmk json2c <keymap>.json -o <keymap>.c

# Before running qmk commands
Replace the keyboard/kinesis folder or the subfolders

# Example
 qmk compile -kb kinesis/nguyenvietyen -km kinesismod
 qmk json2c keymap.json -o keymap.c
