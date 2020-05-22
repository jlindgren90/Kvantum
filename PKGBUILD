# Maintainer: John Lindgren <john@jlindgren.net>
# Maintainer: Bruno Pagani <archange@archlinux.org>

pkgname=kvantum-qt5
pkgver=0.15.3
pkgrel=1
pkgdesc="SVG-based theme engine for Qt5 (including config tool and extra themes)"
arch=(x86_64)
url="https://github.com/tsujan/Kvantum"
license=(GPL)
depends=(qt5-base qt5-svg qt5-x11extras libx11 libxext hicolor-icon-theme kwindowsystem)
makedepends=(cmake qt5-tools)

build() {
  cmake -B ../build -S ../Kvantum -DCMAKE_INSTALL_PREFIX=/usr
  make -C ../build
}

package() {
  make -C ../build DESTDIR="${pkgdir}" install
}
