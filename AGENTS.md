# Agent instructions

## Responsibility

Maintain the ST FingerTip FTM5 touch protocol and contact tracking used by the Xiaomi 13 (fuxi) board.

## Required reading

1. Read this repository's README.
2. Read the [component catalog](https://github.com/OddlyLabs/UniXNU/blob/main/components.toml) entry `FuxiFtsTouch` and the
   fuxi device repository [OddlyLabs/unixnu-fuxi](https://github.com/OddlyLabs/unixnu-fuxi), which holds the board probe
   and the hardware facts with their sources.
3. Read the [porting overview](https://unixnu.com/porting/) and the [input porting page](https://unixnu.com/porting/input).

## Rules

Keep this repository free of board addresses, clocks and pins: those belong to the device repository. Keep the code
pure C without allocation or libc calls; it is compiled with the kernel C flags (`-mgeneral-regs-only`). Do not copy
code from the GPL `fts_spi` driver; restate protocol facts and cite where they come from.

Use `FuxiFtsTouch` for the repository, catalog ID and build references.

## Build and verification

Run both host tests (README) after every change. Report the commands and results, and keep hardware observations
separate from host results.
