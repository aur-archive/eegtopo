# Maintainer: Clemens Brunner <clemens dot brunner at tugraz dot at>
pkgname=eegtopo
pkgver=0.1.0
pkgrel=2
pkgdesc="A program to create montage layouts, topoplots and other graphics based on EEG electrode locations."
arch=('i686' 'x86_64')
url="http://kazemakase.github.com/eegtopo/"
license=('GPL')
depends=('boost' 'cairomm' )
makedepends=('cmake' 'pkgconfig' 'eigen3')
source=(https://github.com/downloads/kazemakase/eegtopo/$pkgname-$pkgver.tar.gz)
md5sums=('61aa13bab214b15ad194cba7c0a53ebf')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  mkdir -p build/cmake
  cd build/cmake
  cmake ../../project
  make
}

package() {
    cd "$pkgdir"
    mkdir -p usr/bin
    cp "$srcdir/$pkgname-$pkgver/build/cmake/eegtopo" "$pkgdir/usr/bin"
}
