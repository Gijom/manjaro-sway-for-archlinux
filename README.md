# Manajaro sway settings for Archlinux

This package aims at reproducing (to the extent it is possible) the [manajaro sway](https://github.com/manjaro-sway/manjaro-sway) community configurations.

The goal is not du duplicate all packages in the AUR but rather to make it more compatible with the Archlinux ecosystem.

**This package is provided without any guarantee, use it at you own risks**

## Changes to the original package

- [x] removed all github workflows
- [x] removed manjaro-base-skel package
- [x] removed the installation of pacman `manjaro-sway-mirrors`
- [x] removed `grimshot` (sway-contrib as alternative ?)
- [x] replaced `sway-services` with AUR `sway-services-git` (:warning: outdated)
- [x] replaced `idlehack` with AUR `idlehack-git`
- [x] replaced `papirus-maia-icon-theme` with AUR `papirus-maia-icon-theme-git`
- [x] replaced `kvantum-theme-matcha` with AUR `kvantum-theme-matcha-git` (:warning: not the same at all, many missing themes)
- [ ] investigate the use of the `sway-contrib` package which seems to provide `grimshot` but enters in conflict with `sway-services-git`
- [ ] investigate if it is possible to replace all sway services with other packages
- [ ] investigate if the AUR `kvantum-theme-matcha-git` package could be used instead of `kvantum-theme-matcha-git` (with replacements of theme configs in `skel` and `/usr/share/sway/themes`)
- [ ] investigate why I get errors because of the --server=3 option (--server alone seem to work)

## Installation

Clone this repository in a folder and from this folder either use the `yay` or `paru` command:

### yay

```
yay -Bi .
```

**Note:** it seems that there is an issue with yay that does not make this solution viable for the moment.

### paru

```
paru -Bi .
```
