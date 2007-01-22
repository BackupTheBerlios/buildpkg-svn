pkgname=terminal
pkgver=0.9.4
src="http://debian.uni-essen.de/misc/GNUstep/Apps/Terminal/Terminal-$pkgver.tar.gz"
build=1dxt

build() {
	cd Terminal-$pkgver

	make
	make INSTALL_ROOT_DIR=${PKG} GNUSTEP_INSTALLATION_DIR=${PKG}/opt/GNUstep/Local install
}
