# Maintainer: Timothy Redaelli <timothy.redaelli@gmail.com>
# Contributor: Vianney le Clément <vleclement AT gmail·com>
# Contributor: Peter Simons <simons@cryp.to>

pkgname=parallel
pkgver=20121022
pkgrel=1
pkgdesc='Shell tool for executing jobs in parallel'
arch=('any')
url='http://www.gnu.org/software/parallel/'
license=('GPL3')
depends=('perl')
source=(http://ftp.gnu.org/gnu/$pkgname/$pkgname-$pkgver.tar.bz2{,.sig})
md5sums=('d0eec562ac3714cf5be74a3bfca856e3'
         '8deded4c2c32a3cdb0f8708d35e949f9')
sha1sums=('3982d4818354f2c2316403a60baa600f10eff26e'
          'ab2ad98d25cb348fec32917532f8b387ea1e4ced')

build() {
  cd "$pkgname-$pkgver"
  source /etc/profile.d/perlbin.sh
  ./configure --prefix=/usr
  make
}

package() {
  cd "$pkgname-$pkgver"
  make DESTDIR="$pkgdir/" install
}

# vim:set ts=2 sw=2 et:
