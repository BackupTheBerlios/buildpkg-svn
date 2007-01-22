pkgname=liboil
pkgver=0.3.9
src="http://liboil.freedesktop.org/download/$pkgname-$pkgver.tar.gz"
build=1dxt

build() {
	cd $pkgname-$pkgver

	./configure --prefix=/usr \
		--sysconfdir=/etc \
		--localstatedir=/var

	make || exit 1
	make DESTDIR=$PKG install
}
