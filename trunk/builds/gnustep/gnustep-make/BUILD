pkgname=gnustep-make
pkgver=1.12.0
src="http://ftp.gnustep.org/pub/gnustep/core/$pkgname-$pkgver.tar.gz"
build=1dxt

build() {
	cd $pkgname-$pkgver

	./configure --prefix=/opt/GNUstep \
		--sysconfdir=/etc \
		--localstatedir=/var

	make -j3 || exit 1
	make special_prefix=$PKG makedir=$PKG/opt/GNUstep/System/Library/Makefiles install
	cd $PKG
	mkdir -p $PKG/etc/profile.d
	cp $PKG/opt/GNUstep/System/Library/Makefiles/GNUstep.{sh,csh} $PKG/etc/profile.d
}
