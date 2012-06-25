# Maintainer: Timothy Redaelli <timothy.redaelli@gmail.com>
# Contributor: Vianney le Clément <vleclement AT gmail·com>
# Contributor: Peter Simons <simons@cryp.to>

pkgname=parallel
pkgver=20120622
pkgrel=1
pkgdesc='A shell tool for executing jobs in parallel'
arch=('any')
url='http://www.gnu.org/software/parallel/'
license=('GPL3')
depends=('perl')
source=(http://ftp.gnu.org/gnu/$pkgname/$pkgname-$pkgver.tar.bz2{,.sig})
md5sums=('b3ee68d13b89aa3ee54ee54b447441be'
         '99c931dbf956be770659621bd7f52419')
sha1sums=('b184a55674ce10e8bf7c65790c2806552eb79577'
          '7b2c3b7440dd4a6107af0333df53f07092d3e5ce')

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
