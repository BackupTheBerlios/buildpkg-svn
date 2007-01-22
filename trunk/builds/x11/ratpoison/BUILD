pkgname=ratpoison
pkgver=1.4.1
src="http://savannah.nongnu.org/download/$pkgname/$pkgname-$pkgver.tar.gz"
build=1dxt

build() {
	cd $pkgname-$pkgver
 
	./configure \
	  --prefix=/usr \
	  --with-x \
	  --with-xterm=$XTERM \
	  || exit
 
	make || exit
	make DESTDIR=${PKG} install || exit
}
