# Maintainer: Timothy Redaelli <timothy.redaelli@gmail.com>
# Contributor: Vianney le Clément <vleclement AT gmail·com>
# Contributor: Peter Simons <simons@cryp.to>

pkgname=parallel
pkgver=20131222
pkgrel=1
pkgdesc='A shell tool for executing jobs in parallel'
arch=('any')
url='http://www.gnu.org/software/parallel/'
license=('GPL3')
depends=('perl')
source=(http://ftp.gnu.org/gnu/$pkgname/$pkgname-$pkgver.tar.bz2{,.sig})
md5sums=('782e594b226454ef58ac4e3d4addaba4'
         'SKIP')
sha1sums=('92d8954a3269aaf95a4abd04ad15e11b1451f2e3'
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
