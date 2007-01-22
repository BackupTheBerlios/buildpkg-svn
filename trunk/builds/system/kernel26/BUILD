pkgname=kernel26
pkgver=2.6.16.18
_arch=i386
src=("http://www.kernel.org/pub/linux/kernel/v2.6/linux-${pkgver}.tar.bz2")
build=1dxt


build() {
	cd linux-${pkgver}
	cat $startdir/config > .config
	make oldconfig || exit
	make bzImage modules || exit 1

	mkdir -p $PKG/{boot,lib/modules,usr/src}
	make INSTALL_MOD_PATH=$PKG modules_install || exit
	cp boot/arch/${_arch}/bzImage $PKG/boot/vmlinuz-${pkgver}
	cp boot/arch/${_arch}/System.map $PKG/boot/System.map-${pkgver}
	make clean

	cd $TMP
	mv linux-${pkgver} $PKG/usr/src/linux-${pkgver}

	mkdir -p $PKG/usr/include
	ln -s $PKG/usr/src/include/linux-${_arch} $PKG/usr/include/linux
	ln -s $PKG/usr/src/include/asm-${_arch} $PKG/usr/include/asm

}
