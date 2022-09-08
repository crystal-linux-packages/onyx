pkgname=onyx
pkgver=1.0
pkgrel=2
pkgdesc="The custom GNOME Session for Crystal Linux"
arch=(any)
url="https://getcryst.al"
license=('GPL')
depends=('gnome' 'gnome-shell-extension-desktop-icons-neo' 'gnome-shell-extension-dash-to-panel' 'gnome-shell-extension-arch-update' 'gnome-shell-extension-gsconnect' 'gnome-shell-extension-caffeine' 'gnome-shell-extension-appindicator' 'xdg-desktop-portal-gtk' 'xdg-desktop-portal-gnome')
source=("00_onyx.gschema.override"
	"onyx.desktop"
	"onyx.json"
	"onyx.session"
	"onyx.session.conf"
	"onyx-wayland.desktop")
md5sums=('SKIP'
	 'SKIP'
	 'SKIP'
	 'SKIP'
	 'SKIP'
	 'SKIP')

package () {
    mkdir -p ${pkgdir}/usr/{lib/systemd/user/gnome-session@onyx.target.d,share/{glib-2.0/schemas,gnome-session/sessions,gnome-shell/modes,wayland-sessions,xsessions}}
    install onyx.session.conf ${pkgdir}/usr/lib/systemd/user/gnome-session@onyx.target.d/onyx.session.conf
    install 00_onyx.gschema.override ${pkgdir}/usr/share/glib-2.0/schemas/00_onyx.gschema.override
    install onyx.session ${pkgdir}/usr/share/gnome-session/sessions/onyx.session
    install onyx.json ${pkgdir}/usr/share/gnome-shell/modes/onyx.json
    install onyx-wayland.desktop ${pkgdir}/usr/share/wayland-sessions/onyx-wayland.desktop
    install onyx.desktop ${pkgdir}/usr/share/xsessions/onyx.desktop
}

