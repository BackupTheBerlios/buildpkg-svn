pkgname=mplayer.app
pkgver=0.4.1
src="http://www.sonappart.net/gnustep/mplayer/Mplayer-0.4-1.tar.gz"
build=1dxt

build() {
	cd mplayerPort/Sources

	sed -i 's|/usr/local/bin|/usr/bin|g' Classes/MplayerInterface.m
	make
	make INSTALL_ROOT_DIR=${PKG} GNUSTEP_INSTALLATION_DIR=${PKG}/opt/GNUstep/Local install
}
