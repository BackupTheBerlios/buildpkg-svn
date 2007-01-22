pkgname=gst-python
pkgver=0.10.4
src="http://gstreamer.freedesktop.org/src/gst-python/$pkgname-$pkgver.tar.gz"
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
