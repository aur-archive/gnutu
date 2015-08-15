# $Id: PKGBUILD 82 2009-07-17 19:56:55Z aaron $
# Contributor: William Rea <sillywilly@gmail.com>

pkgname=gnutu
pkgver=2.5
pkgrel=1.1
pkgdesc="Student planner"
arch=('i686' 'x86_64')
url="http://www.gnutu.devnull.pl"
license=('GPL')
depends=('gtk-sharp-2')
source=(http://gnutu.devnull.pl/download/sources/gnutu-$pkgver.tar.gz)
md5sums=('3b92e24be9ee36e1f7873f17d946a0d2')

build() {
  export MONO_SHARED_DIR=$startdir/src/.wabi
  mkdir -p $MONO_SHARED_DIR

  cd $startdir/src/gnutu-$pkgver
  ./configure --prefix=/usr
  make || return 1
  make DESTDIR=$startdir/pkg install

  rm -rf $MONO_SHARED_DIR
}
 
