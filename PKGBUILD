# Maintainer: Timothy Redaelli <timothy.redaelli@gmail.com>
# Contributor: Vianney le Clément <vleclement AT gmail·com>
# Contributor: Peter Simons <simons@cryp.to>

pkgname=parallel
pkgver=20160522
pkgrel=1
pkgdesc='A shell tool for executing jobs in parallel'
arch=('any')
url='http://www.gnu.org/software/parallel/'
license=('GPL3')
depends=('perl' 'procps')
source=(http://ftp.gnu.org/gnu/$pkgname/$pkgname-$pkgver.tar.bz2{,.sig})
md5sums=('cbf15979ca431452ceecb8e638d5bf13'
         'SKIP')
sha1sums=('d0450ee0d30ff069b9376209b69b388f4ebec00b'
          'SKIP')
validpgpkeys=('CDA01A4208C4F74506107E7BD1AB451688888888')

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
