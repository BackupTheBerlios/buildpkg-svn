pkgname=pygtk
pkgver=2.8.6
src="http://ftp.gnome.org/pub/GNOME/sources/pygtk/2.8/$pkgname-$pkgver.tar.bz2"
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
