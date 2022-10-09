# Maintainer:  echo -n 'bWF0dEBnZXRjcnlzdC5hbAo='     | base64 -d
# Contributor: echo -n 'cmNhbmRhdUBnZXRjcnlzdC5hbA==' | base64 -d

pkgname=onyx
pkgver=1.1
pkgrel=2
pkgdesc="The custom GNOME Session for Crystal Linux"
arch=('any')
url="https://getcryst.al"
license=('GPL')
depends=('baobab' 'eog' 'evince' 'file-roller' 'gdm' 'gedit' 'gnome-backgrounds' 'gnome-calculator' 'gnome-calendar' 'gnome-characters' 'gnome-clocks' 'gnome-color-manager' 'gnome-control-center' 'gnome-disk-utility' 'gnome-font-viewer' 'gnome-keyring' 'gnome-menus' 'gnome-settings-daemon' 'gnome-shell' 'gnome-software' 'gnome-system-monitor' 'gnome-terminal' 'gnome-user-docs' 'gnome-user-share' 'gnome-video-effects' 'gnome-weather' 'grilo-plugins' 'gvfs' 'gvfs-afc' 'gvfs-goa' 'gvfs-google' 'gvfs-gphoto2' 'gvfs-mtp' 'gvfs-nfs' 'gvfs-smb' 'malcontent' 'mutter' 'nautilus' 'orca' 'sushi' 'tracker3-miners' 'vino' 'xdg-user-dirs-gtk' 'gnome-shell-extension-dash-to-panel' 'gnome-shell-extension-arch-update' 'gnome-shell-extension-gsconnect' 'gnome-shell-extension-caffeine' 'gnome-shell-extension-appindicator' 'xdg-desktop-portal-gtk' 'xdg-desktop-portal-gnome')
source=("00_onyx.gschema.override"
	"onyx.desktop"
	"onyx.json"
	"onyx.session"
	"onyx.session.conf"
	"onyx-wayland.desktop")
sha256sums=('1ad2d222c34d316298ff2a8040503e2b0d9a10fbe0f1323fdb11aee8d09992ae'
	    '085c457f80d4cfba7535871726bcb3019679e26e2be7277ecd132d0df852ad6d'
	    'cf387f2fa432a8cd86d1030a41ef6f3904a5ea0eb779e81bd4ed258d855f8d0c'
	    'bb02feab6bd5438e81b22d68c91ed091f8b02f31a36e95bc28e2d8c3e4fa079e'
	    'f4b525ea967ad6da44be70a3ce53bbcdd37d2a4fda9a5c67e4dcc1f02c7cc5ae'
	    '5175d8da7e4036d0c32651d4dbc10c47fa30dae61cacd3512a14636361b682f9')

package () {
    install -Dm 644 onyx.session.conf "${pkgdir}/usr/lib/systemd/user/gnome-session@onyx.target.d/onyx.session.conf"
    install -Dm 644 00_onyx.gschema.override "${pkgdir}/usr/share/glib-2.0/schemas/00_onyx.gschema.override"
    install -Dm 644 onyx.session "${pkgdir}/usr/share/gnome-session/sessions/onyx.session"
    install -Dm 644 onyx.json "${pkgdir}/usr/share/gnome-shell/modes/onyx.json"
    install -Dm 644 onyx-wayland.desktop "${pkgdir}/usr/share/wayland-sessions/onyx-wayland.desktop"
    install -Dm 644 onyx.desktop "${pkgdir}/usr/share/xsessions/onyx.desktop"
}

