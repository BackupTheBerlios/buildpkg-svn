pkgname=buildpkg
pkgver=0.1a
src="http://frogde.sf.net/$pkgname-$pkgver.tar.gz"
build=1dxt

build() {
	cd $pkgname-$pkgver
	mkdir -p $PKG/usr/bin
	install -m755 buildpkg $PKG/usr/bin
	install -m755 genpkg $PKG/usr/bin
}
