# Maintainer: Timothy Redaelli <timothy.redaelli@gmail.com>
# Contributor: Vianney le Clément <vleclement AT gmail·com>
# Contributor: Peter Simons <simons@cryp.to>

pkgname=parallel
pkgver=20120222
pkgrel=2
pkgdesc='A shell tool for executing jobs in parallel'
arch=('any')
url='http://www.gnu.org/software/parallel/'
license=('GPL3')
depends=('perl')
source=("http://ftp.gnu.org/gnu/$pkgname/$pkgname-$pkgver.tar.bz2")
md5sums=('31f211087c7f1c7b99092f6bccaa65ed')
sha1sums=('cf0058a7bbcdeec79a7a43477e7a1aad6fe4d242')

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
