pkgname=addresses
pkgver=0.4.6
src="http://giesler.biz/bjoern/downloads/Addresses-$pkgver.tar.gz"
build=1dxt

build() {
	cd Addresses-0.4.6

	make
	make INSTALL_ROOT_DIR=${PKG} GNUSTEP_INSTALLATION_DIR=${PKG}/opt/GNUstep/Local install
}
