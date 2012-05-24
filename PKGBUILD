# Maintainer: Timothy Redaelli <timothy.redaelli@gmail.com>
# Contributor: Vianney le Clément <vleclement AT gmail·com>
# Contributor: Peter Simons <simons@cryp.to>

pkgname=parallel
pkgver=20120522
pkgrel=1
pkgdesc='A shell tool for executing jobs in parallel'
arch=('any')
url='http://www.gnu.org/software/parallel/'
license=('GPL3')
depends=('perl')
source=(http://ftp.gnu.org/gnu/$pkgname/$pkgname-$pkgver.tar.bz2{,.sig})
md5sums=('521eb454c331b9f7d71199db07aaaa1d'
         '181c40841750e4b22476b246eec0a851')
sha1sums=('bc8118949f900c05ef232c6946c4ebfa779cafed'
          'e3c039c812276142b35d906e5cdea93b3998ffbb')

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
