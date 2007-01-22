pkgname=mpdcon
pkgver=1.1
src="http://studserv.stud.uni-hannover.de/user/64568/MPDCon/MPDCon-$pkgver.tar.gz"
build=1dxt

build() {
	cd MPDCon

	make
	make INSTALL_ROOT_DIR=${PKG} GNUSTEP_INSTALLATION_DIR=${PKG}/opt/GNUstep/Local install
}
