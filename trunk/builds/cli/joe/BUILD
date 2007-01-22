pkgname=joe
pkgver=3.3
src="http://dl.sourceforge.net/sourceforge/$pkgname-editor/$pkgname-$pkgver.tar.gz"
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
