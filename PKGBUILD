# Maintainer: Samed Beyribey <ras0ir@eventualis dot org>
pkgname=kio-gallery3
pkgver=0.1.5
pkgrel=2
pkgdesc="kio-gallery3 implements a kio-slave, a protocol plugin for KDEs I/O system. It makes the content (albums, photos and movies) of a remote Gallery3 system (http://gallery.menalto.com/) directly available inside the KDEs local file hierarchy."
arch=('i686' 'x86_64')
url="http://kde-apps.org/content/show.php/kio-gallery3?content=146835"
license=('LGPL')
depends=('kdebase-runtime' 'qjson')
makedepends=('cmake')
source=(https://api.opensuse.org/public/source/home:arkascha:KDE-4.8/kio-gallery3/$pkgname-$pkgver.tar.bz2)

build() {
  cd "$srcdir/$pkgname-$pkgver"
  mkdir build
  cd build
  cmake .. -DCMAKE_BUILD_TYPE=Release -DCMAKE_SKIP_RPATH=ON -DCMAKE_INSTALL_PREFIX=/usr
  make
}


package() {
  cd "$srcdir/$pkgname-$pkgver/build"
  make DESTDIR="$pkgdir/" install
}

# vim:set ts=2 sw=2 et:
md5sums=('4e2a56c0415ab3d6dc177ac1efaf0895')
