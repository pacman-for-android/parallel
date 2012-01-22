# Maintainer: Timothy Redaelli <timothy.redaelli@gmail.com>
# Contributor: Vianney le Clément <vleclement AT gmail·com>
# Contributor: Peter Simons <simons@cryp.to>

pkgname=parallel
pkgver=20120122
pkgrel=1
pkgdesc='A shell tool for executing jobs in parallel'
arch=('any')
url='http://www.gnu.org/software/parallel/'
license=('GPL3')
depends=('perl')
conflicts=('moreutils')		# provides a script called 'parallel', too
source=("http://ftp.gnu.org/gnu/$pkgname/$pkgname-$pkgver.tar.bz2")
md5sums=('c90077522e95f2c255893fcec55907a8')
sha1sums=('4451129c285f0fc10155949f11b4f523450a599f')

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
