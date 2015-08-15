# Contributor: Petteri Tolonen <petteri.tolonen [at] gmail [dot] com>
# Maintainer: Petteri Tolonen <petteri.tolonen [at] gmail [dot] com>

pkgname=freedink-engine
pkgver=1.08.20101114
pkgrel=2
pkgdesc="A free and enhanced version of the Dink Smallwood game engine"
arch=('i686' 'x86_64')
url="http://www.freedink.org/"
license=('GPL3')
depends=('fontconfig' 'freedink-data' 'sdl_gfx' 'sdl_image' 'sdl_mixer' 'sdl_ttf')
optdepends=('timidity++: MIDI-music support')
conflicts=('freedink-git' 'freedink')
replaces=('freedink-git' 'freedink')
source=(ftp://ftp.gnu.org/gnu/freedink/freedink-$pkgver.tar.gz)
md5sums=('ea045c1dcffa0db076201da7021dec1e')

build() {

   cd $srcdir/freedink-$pkgver/
   
   ./configure --prefix=/usr --disable-embedded-resources
   make || return 1
   make install DESTDIR=$pkgdir || return 1

}
