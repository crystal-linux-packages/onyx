# Maintainer: Matt C <mdc028[at]bucknell[dot]edu>

pkgname=onyx
pkgver=1.2.0
pkgrel=1
pkgdesc="Crystal Linux default desktop setup"
arch=('any')
url="https://github.com/crystal-linux/onyx"
license=('GPL')
source=('inst::git+https://github.com/crystal-linux/onyx')
depends=('gnome-apps-meta' 'budgie-desktop' 'budgie-desktop-view' 'budgie-screensaver' 'budgie-control-center' 'network-manager-applet' 'xorg-server' 'lightdm' 'lightdm-gtk-greeter' 'xdg-utils' 'xdg-desktop-portal-gtk')
conflicts=()
md5sums=('SKIP')
options=(!strip)
install='onyx.install'

package() {

    mkdir -p "${pkgdir}"
    cp -rv inst/usr ${pkgdir}/.
    
}
