# Maintainer: Timothy Redaelli <timothy.redaelli@gmail.com>
# Contributor: Vianney le Clément <vleclement AT gmail·com>
# Contributor: Peter Simons <simons@cryp.to>

pkgname=parallel
pkgver=20171222
pkgrel=1
pkgdesc='A shell tool for executing jobs in parallel'
arch=('any')
url='http://www.gnu.org/software/parallel/'
license=('GPL3')
depends=('perl' 'procps')
source=(https://ftp.gnu.org/gnu/$pkgname/$pkgname-$pkgver.tar.bz2{,.sig})
md5sums=('ca03691d1eba5c953d03a9d155174e72'
         'SKIP')
sha1sums=('e8632264794c3408cf58502bdc187205638de7a2'
          'SKIP')
validpgpkeys=('CDA01A4208C4F74506107E7BD1AB451688888888')

build() {
  cd parallel-$pkgver
  ./configure --prefix=/usr
  make
}

package() {
  cd parallel-$pkgver
  make DESTDIR="$pkgdir/" install
}

# vim:set ts=2 sw=2 et:
