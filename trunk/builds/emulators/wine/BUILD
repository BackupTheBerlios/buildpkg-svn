pkgname=wine
pkgver=0.9.28
src="http://ibiblio.org/pub/linux/system/emulators/wine/$pkgname-$pkgver.tar.bz2"
build=1dxt

build() {
	cd $pkgname-$pkgver
	./configure --with-x --disable-debug --prefix=/usr --sysconfdir=/etc --localstatedir=/var
	make DESTDIR=$PKG || exit
	make DESTDIR=$PKG install || exit
}
