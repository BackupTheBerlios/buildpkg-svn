pkgname=gtk-qt-engine
pkgver=0.6
src="http://www.freedesktop.org/~davidsansome/$pkgname-$pkgver.tar.bz2"
build=1dxt

build() {
	cd $pkgname-$pkgver

	./configure \
		--prefix=/usr \
		--sysconfdir=/etc \
		--program-prefix="" \
		--program-suffix=""

	make -j3 || exit 1
	make DESTDIR=$PKG install
}
