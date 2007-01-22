pkgname=glibc
pkgver=2.3.6
src="http://ftp.gnu.org/gnu/glibc/$pkgname-$pkgver.tar.bz2"
build=2dxt

build() {
	cd $pkgname-$pkgver
	tar -jxvf $startdir/glibc-libidn-$pkgver.tar.bz2
	tar -jxvf $startdir/glibc-linuxthreads-$pkgvar.tar.bz2

	# Patches:
	# Use old-style locale directories rather than a single (and strangely
	# formatted) /usr/lib/locale/locale-archive file
	zcat $startdir/glibc.locale.no-archive.diff.gz | patch -p1 --verbose || exit 1

	# Fix XMMS/X crash caused by interaction with nVidia drivers
	zcat $startdir/glibc.tls.crashfix.diff.gz | patch -p1 --verbose || exit 1

	# Fix NIS netgroups
	zcat $startdir/glibc.nis-netgroups.diff.gz | patch -p1 --verbose || exit 1


	# Update the timezone information, or a lot of people will be
	# very unhappy...
	if [ $CVSVER = 2.3.6 ]; then
		echo "Updating timezone information (tzdata2005c/tzcode2005c):"  
		rm -r timezone
		tar jxvf $startdir/tzdata2005ctzcode2005c.tar.bz2
	fi

	$ Creating the build directory
	mkdir build-glibc-$pkgver
	cd build-glibc-$pkgver

	../configure \
		--prefix=/usr \
		--enable-kernel=2.6.4 \
		--with-headers=/usr/src/linux-${HEADERSTWOSIX}/include \
		--enable-add-ons=libidn,nptl \
		--with-tls \
		--with-__thread \
		--without-cvs


make -j3
make install install_root=$PNPTL
make localedata/install-locales install_root=$PNPTL


	./configure --prefix=/usr \
		--sysconfdir=/etc \
		--localstatedir=/var \
		--enable-python

	make -j3 || exit 1
	make DESTDIR=$PKG install
}
