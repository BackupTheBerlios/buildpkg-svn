pkgname=jigs
pkgver=1.5.5
src="http://www.gnustep.it/jigs/Download/$pkgname-$pkgver.tar.gz"
build=1dxt

build() {
	cd Addresses-0.4.6

	make
	make INSTALL_ROOT_DIR=${PKG} GNUSTEP_INSTALLATION_DIR=${PKG}/opt/GNUstep/Local install
}
