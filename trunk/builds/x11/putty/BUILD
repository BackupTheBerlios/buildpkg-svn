pkgname=putty
pkgver=0.58
src="http://the.earth.li/~sgtatham/putty/latest/$pkgname-$pkgver.tar.gz"
build=1dxt

build() {
	cd $pkgname-$pkgver/unix

	make -j3 -f Makefile.gtk || exit 1
	mkdir -p $PKG/usr/bin
	mkdir -p $PKG/usr/man/man1
	make -f Makefile.gtk prefix=$PKG/usr install
	cd ..

}
