# Maintainer: Arda Atci<phystecharda@gmail.com>
pkgname=dmenu-phyOS
pkgver=4.9
pkgrel=1
pkgdesc="dmenu build for phyOS"
arch=(x86_64)
url="git://github.com/PhyTech-R0/dmenu-phyOS"
license=('MIT')
depends=('coreutils' 'fontconfig' 'freetype2' 'glibc' 'fontconfig' 'libx11' 'libxft' 'libxinerama')
makedepends=('git' 'make')
optdepends=('st')
provides=("dmenu")
conflicts=("dmenu")
options=('zipman')
source=('git://github.com/PhyTech-R0/dmenu-phyOS')
md5sums=('SKIP')

build() {
	cd $pkgname
	make X11INC=/usr/include/X11 X11LIB=/usr/lib/X11
}


package() {
	cd "$pkgname"
	make PREFIX=/usr DESTDIR="$pkgdir/" install
	install -m644 -D LICENSE $pkgdir/usr/share/licenses/$pkgname/LICENSE
}
