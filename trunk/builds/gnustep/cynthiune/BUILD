pkgname=cynthiune
pkgver=0.9.5
src="http://organact.mine.nu/~wolfgang/cynthiune/Cynthiune-$pkgver.tar.gz"
build=1dxt

build() {
	cd Cynthiune-$pkgver

	make disable-mod=yes disable-windowsmedia=yes disable-musepack=yes
	make disable-mod=yes disable-windowsmedia=yes disable-musepack=yes INSTALL_ROOT_DIR=${PKG} GNUSTEP_INSTALLATION_DIR=${PKG}/opt/GNUstep/Local install
}
