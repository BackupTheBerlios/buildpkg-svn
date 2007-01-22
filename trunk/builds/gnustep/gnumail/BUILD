pkgname=gnumail
pkgver=1.2.0pre1
src="http://www.collaboration-world.com/cgi-bin/project/download.cgi/GNUMail-$pkgver.tar.gz?rid=97"
build=1dxt

build() {
	cd GNUMail

	sed -i 's|<AddressBook/|<Addresses/|g' \
		Bundles/Filtering/FilterEditorWindowController.m

	sed -i 's|<AddressBook/|<Addresses/|g' \
		AddressBookController.h


	make || exit
	make INSTALL_ROOT_DIR=${PKG} GNUSTEP_INSTALLATION_DIR=${PKG}/opt/GNUstep/Local install
}
