# Maintainer: speps <speps dot aur dot archlinux dot org>

pkgname=zam-plugins
pkgver=3.5
pkgrel=1
pkgdesc="Collection of LV2/LADSPA audio plugins for high quality processing"
arch=('i686' 'x86_64')
url="http://www.zamaudio.com/?p=976"
license=('GPL')
groups=('lv2-plugins' 'ladspa-plugins')
depends=('libgl')
makedepends=('jack' 'liblo')
source=("https://github.com/zamaudio/zam-plugins/archive/$pkgver.tar.gz")
md5sums=('fdcb0b4f072791f83b9b5968aab78ebe')

build() {
  cd $pkgname-$pkgver
  make PREFIX=/usr
}

package() {
  cd $pkgname-$pkgver
  make PREFIX=/usr DESTDIR="$pkgdir/" install
}
