# Maintainer: Jonas Strassel <info@jonas-strassel.de>
# TODO: Check sway-contrib package which seems to probide grimshot and a systemd script of sway services (which seem outdated)
pkgname=manjaro-sway-settings
pkgver=17.1.0
pkgrel=11
arch=('any')
_pkgbase=desktop-settings
url="https://github.com/Manjaro-Sway/$_pkgbase"
license=('GPL')
pkgdesc='Manjaro Sway Settings'
groups=('sway-manjaro')
depends=(
#    'manjaro-base-skel'
    'waybar'            # configurable bar
    'brightnessctl'     # cli to control brightness
    'mako'              # desktop notifications
    'sway'              # window manager
    'rofi-wayland'      # launcher application
#    'sway-services-git'     # systemd services for sway
    'wl-clip-persist'   # persists clipboard content between containers
    'swayidle'          # idle management daemon
    'grim'              # screenshot tool
    'slurp'             # helper for grim
    'wob'               # wayland overlay bar for brightness and volume
    'foot'              # terminal application
    'foot-terminfo'     # terminal info for foot
    'jq'                # json parsing and manipulation
    'calcurse'          # tui calendar application
    'lm_sensors'        # display sensor information
    'wf-recorder'       # screen recording util
    'wl-clipboard'      # copy/paste utilities for wayland
    'nwg-wrapper'       # conky like onscreen information'
    'noto-fonts-emoji'  # emoji font (e.g. weather icons)
    'btop'              # system monitor
    'swappy'            # screenshot editing tool
#    'grimshot'          # screenshot tool
    'inotify-tools'     # file watchers etc
    'bluetuith'         # bluetooth management tool
    'swayr'             # lru window switcher for sway
    'bc'                # basic tiny calculation util
    'xdg-terminal-exec' # upcoming execute in terminal xdg standard
#    'idlehack-git'          # commented out 2026-06-19: outdated local AUR git package (0.r19-1 -> latest-commit); review PKGBUILD before re-enabling
    'dex'               # executes desktop entries on autostart
    'swaybg'            # wallpaper setter
    'rofimoji'          # emoji picker
    ## theme
    'kvantum'                 # theme engine for qt
    'kvantum-qt5'             # theme engine for qt (qt 5 support)
    'ttf-jetbrains-mono-nerd' # default monospace font
    'ttf-roboto'              # default font
#    'papirus-maia-icon-theme-git' # commented out 2026-06-19: package name appears in public June 2026 AUR compromise lists; review PKGBUILD/source before re-enabling
    'phinger-cursors'         # default cursor theme
#    'matcha-gtk-theme'        # commented out 2026-06-19: outdated local AUR package (2023.10.30-2 -> 2025.04.11-3); review PKGBUILD before re-enabling
    'kvantum-theme-matcha-git'    # default kvantum (kde etc.) theme
)
makedepends=('git')
optdepends=(
    'qutebrowser: a keyboard-centric browser'
#    'flashfocus: better flashing on focus changes' # commented out 2026-06-19: package name appears in public June 2026 AUR compromise lists; review PKGBUILD/source before re-enabling
    'waylock: reference lockscreen for ext-session-lock-v1'
    'gtklock: lockscreen based on gtkgreet'
    'swaylock: minimalistic lockscreen'
    'swaylock-effects: minimalistic lockscreen with fancy effects'
    'wlsunset: time & place based light temperature'
    'way-displays: automated display management'
    'autotiling: automated tiling'
    'sworkstyle: dynamic workspace names (icons) in waybar'
    'nwg-wrapper: conky like onscreen information'
    'cliphist: clipboard manager'
    'swaycwd: open here helper'
    'zeit: a simple time tracker'
    'dex: execute DesktopEntry files on autostart'
    'poweralertd: battery and power notifications'
    'wluma: adaptive brightness based on screen contents and ALS'
    'valent: kdeconnect-like tool without the kde bloat'
    'pacseek: package manager tui'
    'openbsd-netcat: network utility (e.g. for termbin)'
    'pacman-log-orphans-hook: pacman hook to log orphaned packages'
    'pcmanfm-qt: file manager'
)
conflicts=('manjaro-sway-settings-git')
provides=('manjaro-desktop-settings')
_sourcemd5=1648e898d71d2ff05fbc07844e7e2af4
source=(
    "$pkgname-$pkgver.tar.gz::${url}/archive/${pkgver}.tar.gz"
    "https://github.com/arcolinux/arcolinux-on-the-road/raw/cfbcc902b9520cc4ff73584dd80f34c54a158c75/root/usr/local/bin/skel"
)
md5sums=(
    "$_sourcemd5"                      # desktop settings
    "3ce84d692c6fdbaf31e1b602bc890aa4" # skel update script from arcolinux
)
install=.install

package() {
    install -d "$pkgdir"/etc
    install -d "$pkgdir"/usr/bin
    cp -r $_pkgbase-$pkgver/community/sway/etc/* "${pkgdir}/etc/"
    cp -r $_pkgbase-$pkgver/community/sway/usr/* "${pkgdir}/usr/"
    install -D -m 755 skel "${pkgdir}/usr/bin/skel"
}
