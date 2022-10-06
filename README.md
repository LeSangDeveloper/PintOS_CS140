# PintOS_CS140
This project is a study case for Operating System class CS140

# Installing

Cause I used Ubuntu to study and qemu to learn so I just modify to appriate to my case.

## Prequistitute

` sudo apt-get install gcc binutils perl make qemu gdb `

## Set GDBMACROS

Open the script `pintos-gdb` (in $YOUR_PINTOS_FOLDER/src/utils) in any text editor. Find the variable GDBMACROS and set it to point to $YOUR_PINTOS_FOLDER/src/misc/gdb-macros .

## Compile Utilities

In `$YOUR_PINTOS_FOLDER/src/utils` run `make`

If you get an error saying `Undefined reference to ‘floor' `, make the following changes; edit `Makefile` in the current directory and replace `LDFLAGS = -lm` by `LDLIBS = -lm`. Recompile now, it will work.


## Edit Make.vars in /threads

Edit the file `Make.vars` in the `threads` directory ( $YOUR_PINTOS_FOLDER/src/utils ); change the last line to: SIMULATOR = --qemu cause I used QEMU

## Compile Pintos kernel

Change to the 'threads' directory, if not already there, and run 'make' to compile the pintos kernel.

## Edit the pintos utility

Make these changes in the `pintos` file at `$YOUR_PINTOS_FOLDER/src/utils`:

```
a) On line number 103, change 'bochs' to 'qemu'.
b) On line number 259, change 'kernel.bin' to the actual path at '$HOME/stanford/pintos/src/threads/build/kernel.bin'.
```

## Edit pintos.pm file

Open the file `$YOUR_PINTOS_FOLDER/src/utils/Pintos.pm` in the editor and at line number 362, change "loader.bin" to the actual path to the file at `$YOUR_PINTOS_FOLDER/src/threads/build/loader.bin`.

## Create qemu link

ln -s qemu-system-x86_64 qemu

## Create PATH

add your folder to PATH environment

