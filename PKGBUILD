# Maintainer: Jan Boelsche <jan@lagomorph.de>
pkgname=libphidget22extra
pkgver=1.0.0.20180406
pkgrel=1
pkgdesc="extra user-space access library for the Phidget devices"
url="https://www.phidgets.com/docs/OS_-_Linux"
provides=('libphidgetextra')
arch=('x86_64')
license=('GPL')
depends=('libphidget22')
source=("https://www.phidgets.com/downloads/phidget22/libraries/linux/$pkgname/$pkgname-$pkgver.tar.gz")
sha256sums=('0492d65882f08ea8f0de98c5a23c8d015361f30c1c3d6c48182e192096024f77')

build() {
  cd $pkgname-$pkgver
  ./configure --prefix=/usr
  make
}

package() {
   cd $pkgname-$pkgver
   make DESTDIR="$pkgdir/" install
}
