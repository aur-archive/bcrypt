# Contributor: Benjamin S. <bs at kniegeil dot de>
# Maintainer: Ruben Reyes <usa dot rreyes at gmail dot com>
pkgname=bcrypt
pkgver=1.1
pkgrel=4
pkgdesc="Blowfish File Encryption"
arch=(i686 x86_64)
license=('custom')
url="http://bcrypt.sf.net"
depends=('zlib')
source=(http://bcrypt.sourceforge.net/$pkgname-$pkgver.tar.gz)
md5sums=('8ce2873836ccd433329c8df0e37e298c')

build() {
      cd $srcdir/$pkgname-$pkgver
      sed -i 's/${PREFIX}\/man/${PREFIX}\/share\/man/g' Makefile
      make
}

package(){
      cd $srcdir/$pkgname-$pkgver
      make PREFIX=$pkgdir/usr install
      install -Dm644 LICENSE $pkgdir/usr/share/licenses/bcrypt/LICENSE
}
