# Maintainer:  <alexander@Alexander-PC>
pkgname=cryptobox-c
pkgver=1.1.3
pkgrel=1
pkgdesc=""
arch=('i686' 'x86_64')
url="https://github.com/wireapp/cryptobox-c.git"
license=('GPLv3')
groups=()
depends=("libsodium")
makedepends=("rust")
source=("https://github.com/wireapp/cryptobox-c/archive/v$pkgver.zip")
md5sums=('d2a32b0c84fc3a337d13f5608d34b03d')
noextract=()


build() {
  cd "$srcdir/$pkgname-$pkgver"

  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"

  mkdir -p $pkgdir/usr/lib
  mkdir -p $pkgdir/usr/include

  make TARGET_LIB="$pkgdir/usr/lib" TARGET_INCLUDE="$pkgdir/usr/include" install
}

# vim:set ts=2 sw=2 et:
