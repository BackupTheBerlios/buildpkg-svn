pkgname=gnustep-back
pkgver=0.10.3
src="http://ftp.gnustep.org/pub/gnustep/core/$pkgname-$pkgver.tar.gz"
build=2dxt

build() {
	cd $pkgname-$pkgver

	./configure --prefix=/opt/GNUstep \
		--sysconfdir=/etc \
		--localstatedir=/var \
		--enable-graphics=xlib \
		--with-name=xlib \
		--enable-graphics=art \
		--with-name=art \
		--disable-glitz


	make || exit 1
	make INSTALL_ROOT_DIR=${PKG} GNUSTEP_INSTALLATION_DIR=${PKG}/opt/GNUstep/System install
}
