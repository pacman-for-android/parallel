# Maintainer: Timothy Redaelli <timothy.redaelli@gmail.com>
# Contributor: Vianney le Clément <vleclement AT gmail·com>
# Contributor: Peter Simons <simons@cryp.to>

pkgname=parallel
pkgver=20140722
pkgrel=1
pkgdesc='A shell tool for executing jobs in parallel'
arch=('any')
url='http://www.gnu.org/software/parallel/'
license=('GPL3')
depends=('perl')
source=(http://ftp.gnu.org/gnu/$pkgname/$pkgname-$pkgver.tar.bz2{,.sig})
md5sums=('c9179f12dee5858f98b5d34147a6fe8a'
         'SKIP')
sha1sums=('3f92a1069e068cda11cab0e0c698919991e470a0'
          'SKIP')

build() {
  cd "$pkgname-$pkgver"
  ./configure --prefix=/usr
  make
}

package() {
  cd "$pkgname-$pkgver"
  make DESTDIR="$pkgdir/" install
}

# vim:set ts=2 sw=2 et:
