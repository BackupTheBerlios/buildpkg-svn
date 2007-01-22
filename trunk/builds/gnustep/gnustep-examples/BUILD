pkgname=gnustep-examples
pkgver=1.0.0
src="ftp://ftp.gnustep.org/pub/gnustep/core/$pkgname-$pkgver.tar.gz"
build=1dxt

build() {
	cd $pkgname-$pkgver

	make || exit
	make GNUSTEP_INSTALL_ROOT=${PKG} \
	GNUSTEP_INSTALLATION_DIR=${PKG}/opt/GNUstep/Local install
}
