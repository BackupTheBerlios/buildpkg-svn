pkgname=gnustep-base
pkgver=1.12.0
src="http://ftp.gnustep.org/pub/gnustep/core/$pkgname-$pkgver.tar.gz"
build=1dxt

build() {
	cd $pkgname-$pkgver

	./configure --prefix=/opt/GNUstep \
		--sysconfdir=/etc \
		--localstatedir=/var

	make || exit 1
	make INSTALL_ROOT_DIR=${PKG} GNUSTEP_INSTALLATION_DIR=${PKG}/opt/GNUstep/System install
}
