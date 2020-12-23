# Maintainer:  twa022 <twa022 at gmil dot com>
# Contributor: Thanos Apostolou <thanosapostolou@outlook.com>
# Contributor: Cedric Leporcq <cedric at gmail dot com>

pkgname=xfce4-windowck-plugin
pkgver=0.4.10
pkgrel=1
pkgdesc="Xfce panel plugin which allows to put the maximized window title and buttons on the panel."
arch=('i686' 'x86_64')
url="https://github.com/invidian/xfce4-windowck-plugin"
license=('GPL3')
depends=('xfce4-panel<4.17.0' 'libwnck')
makedepends=('intltool' 'xfce4-dev-tools' 'python' 'imagemagick')
options=('!libtool')
source=("$pkgname-$pkgver.tar.gz::https://github.com/invidian/$pkgname/archive/v$pkgver.tar.gz")
sha256sums=('ff12ae63b26f5d62c839e9c15b329de2b1f372f105fbc063281a98a62097cac3')

build() {
  cd "$srcdir/${pkgname}-$pkgver"
  ./autogen.sh --prefix=/usr
  make
}

package() {
  cd "$srcdir/${pkgname}-$pkgver"
  make DESTDIR="$pkgdir" install
}
