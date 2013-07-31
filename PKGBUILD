# Maintainer: Timothy Redaelli <timothy.redaelli@gmail.com>
# Contributor: Vianney le Clément <vleclement AT gmail·com>
# Contributor: Peter Simons <simons@cryp.to>

pkgname=parallel
pkgver=20130722
pkgrel=1
pkgdesc='A shell tool for executing jobs in parallel'
arch=('any')
url='http://www.gnu.org/software/parallel/'
license=('GPL3')
depends=('perl')
source=(http://ftp.gnu.org/gnu/$pkgname/$pkgname-$pkgver.tar.bz2{,.sig}
        fix-pod-numbers.patch)
md5sums=('ddb92b545af782b4d6288c65ef28847e'
         'SKIP'
         '2b5e03baf585de642885062f177efc03')
sha1sums=('d794ac9c2c0a73d430b9ae2ebbbd07e4eb2fcaf0'
          'SKIP'
          '0def90e91269073213a0e78b34754c95b7ddd4f2')

prepare() {
  cd "$pkgname-$pkgver"
  patch -p0 -i "$srcdir/fix-pod-numbers.patch"
}

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
