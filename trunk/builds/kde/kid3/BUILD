pkgname=kid3
pkgver=0.3.0beta1
src="http://thunar.xfce.org/download/releases/beta1/Thunar-$pkgver.tar.bz2"
build=1dxt

build() {
	cd Thunar-$pkgver

	./configure --prefix=/usr \
		--sysconfdir=/etc \
		--localstatedir=/var \
		--with-volume-manager=hal

	make -j3 || exit 1
	make DESTDIR=$PKG install
}
