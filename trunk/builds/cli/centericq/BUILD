pkgname=centericq
pkgver=4.21.0
src="http://www.konst.org.ua/download/$pkgname-$pkgver.tar.gz"
build=1dxt

build() {
	cd $pkgname-$pkgver
	./configure --prefix=/usr --sysconfdir=/etc --localstatedir=/var --disable-x
	make DESTDIR=$PKG || exit
	make DESTDIR=$PKG install || exit
}
