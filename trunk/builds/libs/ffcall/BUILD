pkgname=ffcall
pkgver=1.10
src="ftp://ftp.santafe.edu/pub/gnu/$pkgname-$pkgver.tar.gz"
build=1dxt

build() {
	cd $pkgname-$pkgver

	./configure --prefix=/usr \
		--sysconfdir=/etc \
		--localstatedir=/var

	make || exit 1
	make DESTDIR=$PKG install
}
