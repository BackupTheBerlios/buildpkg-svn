pkgname=torsmo
pkgver=0.18
src="http://dl.sourceforge.net/sourceforge/torsmo/$pkgname-$pkgver.tar.gz"
build=2jtn

build() {
	cd $pkgname-$pkgver

	./configure --prefix=/usr \
		--localstatedir=/var \
		--sysconfdir=/etc \
		--program-suffix="" \
		--program-prefix=""

	make || exit
	make DESTDIR=${PKG} install
	mkdir -p ${PKG}/etc
	cp torsmorc.sample ${PKG}/etc
}
