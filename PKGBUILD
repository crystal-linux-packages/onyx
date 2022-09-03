_pkgname=onyx
pkgname=onyx
pkgver=1.0
pkgrel=1
pkgdesc="The custom gnome session for crystal linux"
arch=(any)
url="https://getcryst.al"
license=('GPL')
depends=('gnome-shell' 'gnome-shell-extension-desktop-icons-neo' 'gnome-shell-extension-dash-to-panel' 'gnome-shell-extension-arch-update' 'gnome-shell-extension-gsconnect' 'gnome-shell-extension-caffeine' 'gnome-shell-extension-appindicator' 'gnome-shell-extension-space-bar')
provides=("$_pkgname")
source=("00_onyx.gschema.override"
	"onyx.desktop"
	"onyx.json"
	"onyx.session"
	"onyx.session.conf"
	"onyx-wayland.desktop")
md5sums=('SKIP')

package () {
    install onyx.session.conf ${pkgdir}/usr/lib/systemd/user/gnome-session@onyx.target.d/onyx.session.conf
    install 00_onyx.gschema.override ${pkgdir}/usr/share/glib-2.0/schemas/00_onyx.gschema.override
    install onyx.session ${pkgdir}/usr/share/gnome-session/sessions/onyx.session
    install onyx.json ${pkgdir}/usr/share/gnome-shell/modes/onyx.json
    install onyx-wayland.desktop ${pkgdir}/usr/share/wayland-sessions/onyx-wayland.desktop
    install onyx.desktop ${pkgdir}/usr/share/xsessions/onyx.desktop
}

