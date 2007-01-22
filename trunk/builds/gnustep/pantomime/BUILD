pkgname=pantomime
pkgver=1.2.0pre1
src="http://www.collaboration-world.com/cgi-bin/project/download.cgi/Pantomime-$pkgver.tar.gz?rid=96"
build=1dxt

build() {
	cd Pantomime

	make
	make INSTALL_ROOT_DIR=${PKG} GNUSTEP_INSTALLATION_DIR=${PKG}/opt/GNUstep/System install
}
