pkgname=exo
pkgver=0.3.1.6beta1
src="http://thunar.xfce.org/download/releases/beta1/$pkgname-$pkgver.tar.bz2"
build=2dxt

build() {
	cd $pkgname-$pkgver

	./configure --prefix=/usr \
		--sysconfdir=/etc \
		--localstatedir=/var \
		--enable-python

	make -j3 || exit 1
	make DESTDIR=$PKG install
}
