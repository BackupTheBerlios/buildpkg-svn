pkgname=mpd
pkgver=0.11.5
src="http://mercury.chem.pitt.edu/~shank/$pkgname-$pkgver.tar.gz"
build=1dxt

build() {
	cd $pkgname-$pkgver
	./configure --prefix=/usr --sysconfdir=/etc --localstatedir=/var
	make DESTDIR=$PKG || exit
	make DESTDIR=$PKG install || exit

	mkdir -p $PKG/etc/rc.d
	cat $startdir/rc.mpd > $PKG/etc/rc.d/rc.mpd
}
