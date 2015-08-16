# Maintainer: Rohit R <rrohit.rht@gmail.com>
# Contributor: Anton Bazhenov <anton.bazhenov at gmail>
# Contributor: Arjun Shankar <arjunsha@gmail.com>

pkgname=libmatheval
pkgver=1.1.11
pkgrel=2
pkgdesc="A library to parse and evaluate symbolic expressions input as text"
arch=('i686' 'x86_64')
url="http://www.gnu.org/software/libmatheval/"
license=('GPL3')
depends=()
makedepends=('guile1.8')
source=(http://ftp.gnu.org/gnu/$pkgname/$pkgname-$pkgver.tar.gz)
md5sums=('595420ea60f6ddd75623847f46ca45c4')

build() {
  cd "${srcdir}"/${pkgname}-${pkgver}
  ./configure --prefix=/usr
  make
}

package() {
  cd "${srcdir}"/${pkgname}-${pkgver}
  make DESTDIR="${pkgdir}" install
  install -Dm644 COPYING "$pkgdir/usr/share/licenses/$pkgname/COPYING"
}
