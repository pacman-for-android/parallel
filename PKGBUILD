# Maintainer: Timothy Redaelli <timothy.redaelli@gmail.com>
# Contributor: Vianney le Clément <vleclement AT gmail·com>
# Contributor: Peter Simons <simons@cryp.to>

pkgname=parallel
pkgver=20121222
pkgrel=1
pkgdesc='A shell tool for executing jobs in parallel'
arch=('any')
url='http://www.gnu.org/software/parallel/'
license=('GPL3')
depends=('perl')
source=(http://ftp.gnu.org/gnu/$pkgname/$pkgname-$pkgver.tar.bz2{,.sig})
md5sums=('7ad8fdf38a6e36150e76c4deb58c0e1b'
         '09f4e4dc98567778cfd51394f22807d7')
sha1sums=('e9823e44b01eb99a3e8737af858f19d28c7df924'
          '9f96dfd61cdce87be094323f4ee24f4aed9db275')

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
