pkgname=jpilot
pkgver=0.99.8
src=(http://jpilot.org/$pkgname-$pkgver.tar.gz http://www.jpilot.org/patch.jpilot-sync http://www.jpilot.org/patch.0.99.8-memory)

build=1dxt

build() {
	cd $pkgname-$pkgver
	cat $TMP/patch.0.99.8-memory | patch -p0
	cat $TMP/patch.jpilot-sync | patch -p0

	./configure --prefix=/usr \
		--sysconfdir=/etc \
		--localstatedir=/var \
		--enable-gtk2

	make -j3 || exit 1
	make DESTDIR=$PKG install

}
