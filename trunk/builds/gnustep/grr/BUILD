pkgname=grr
pkgver=0.6.2
src="http://www.unix-ag.uni-kl.de/~guenther/downloads/Grr-$pkgver.tar.gz"
build=1dxt

build() {
	cd Grr-$pkgver

	make || exit
	make GNUSTEP_INSTALL_ROOT=${PKG} GNUSTEP_INSTALLATION_DIR=${PKG}/opt/GNUstep/Local install
}
