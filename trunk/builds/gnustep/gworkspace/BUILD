pkgname=gworkspace
pkgver=0.8.2
src="http://www.gnustep.it/enrico/gworkspace/$pkgname-$pkgver.tar.gz"
build=1dxt

build() {
	cd GWorkspace-$pkgver

	./configure \
		--prefix=/opt/GNUstep \
		--sysconfdir=/etc \
		--localstatedir=/var
	make
	make INSTALL_ROOT_DIR=${PKG} GNUSTEP_INSTALLATION_DIR=${PKG}/opt/GNUstep/System install
}
