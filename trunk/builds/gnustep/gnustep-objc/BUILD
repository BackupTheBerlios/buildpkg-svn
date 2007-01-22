pkgname=gnustep-objc
pkgver=1.4.0
src="ftp://ftp.gnustep.org/pub/gnustep/libs/$pkgname-$pkgver.tar.gz"
build=1dxt

build() {
	cd $pkgname-$pkgver

	make || exit
	make GNUSTEP_INSTALLATION_DIR=${PKG}/opt/GNUstep/System install
}
