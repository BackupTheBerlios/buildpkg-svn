pkgname=gstreamer
pkgver=0.10.6
src="http://gstreamer.freedesktop.org/src/$pkgname/$pkgname-$pkgver.tar.gz"
build=1dxt

build() {
	cd $pkgname-$pkgver

	./configure --prefix=/usr \
		--localstatedir=/var \
		--sysconfdir=/etc \
		--program-suffix="" \
		--program-prefix=""

	make || exit
	make DESTDIR=${PKG} install
}
