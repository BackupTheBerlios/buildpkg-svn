pkgname=buildpkg
pkgver=0.2
src="http://frogde.sf.net/buildpkg/$pkgname-$pkgver.tar.gz"
build=1dxt

build() {
	cd $pkgname-$pkgver
	mkdir -p $PKG/usr/bin
	install -m755 buildpkg $PKG/usr/bin
	install -m755 genpkg $PKG/usr/bin
}
