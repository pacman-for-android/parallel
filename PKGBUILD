# Maintainer: Timothy Redaelli <timothy.redaelli@gmail.com>
# Contributor: Vianney le Clément <vleclement AT gmail·com>
# Contributor: Peter Simons <simons@cryp.to>

pkgname=parallel
pkgver=20111222
pkgrel=1
pkgdesc='A shell tool for executing jobs in parallel'
arch=('any')
url='http://www.gnu.org/software/parallel/'
license=('GPL3')
depends=('perl')
conflicts=('moreutils')		# provides a script called 'parallel', too
source=("http://ftpmirror.gnu.org/$pkgname/$pkgname-$pkgver.tar.bz2")
md5sums=('cddba502666d4c6658a59060fed854f3')
sha1sums=('6d4896b900f5330f8b4108d6fbec80633da33538')

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
