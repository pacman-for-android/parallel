# Maintainer: Timothy Redaelli <timothy.redaelli@gmail.com>
# Contributor: Vianney le Clément <vleclement AT gmail·com>
# Contributor: Peter Simons <simons@cryp.to>

pkgname=parallel
pkgver=20150522
pkgrel=1
pkgdesc='A shell tool for executing jobs in parallel'
arch=('any')
url='http://www.gnu.org/software/parallel/'
license=('GPL3')
depends=('perl' 'procps')
source=(http://ftp.gnu.org/gnu/$pkgname/$pkgname-$pkgver.tar.bz2{,.sig})
md5sums=('baa13d9ed0caad76004e9fe9b9b78c72'
         'SKIP')
sha1sums=('2a60a866ec8d0116d277718b47a2da26eaf4e961'
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

  # FIXME
  ln -sf parallel "$pkgdir/usr/bin/sem"
}

# vim:set ts=2 sw=2 et:
