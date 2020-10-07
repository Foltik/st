# Maintainer: Jack Foltz <jack@foltz.io>
pkgname=st
pkgver=0.8.4
pkgrel=1
pkgdesc="Simple Terminal (Foltik's Patches)"
arch=('i686' 'x86_64' 'armv7h')
url="https://st.suckless.org"
license=('MIT')
depends=('libxft')

pkgver() {
	cd ..
	grep "VERSION = " config.mk | awk '{print $3}'
}

build() {
	cd ..
	make
}

package() {
	cd ..
	make PREFIX=/usr DESTDIR="$pkgdir" install
	install -m644 -D LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
	install -m644 -D README "$pkgdir/usr/share/doc/$pkgname/README"
}
