pkgname=tir
pkgver=0.2.1
pkgrel=1
pkgdesc="Terminal Image Renderer"
arch=('i686' 'x86_64')
url=https://github.com/ikaros/tir
license=(BSD)
makedepends=('go')
provides=('tir')
source=("${pkgname}-${pkgver}.tar.gz::https://github.com/ikaros/${pkgname}/archive/v${pkgver}.tar.gz")
sha1sums=('08c807785ae830011ca19a216d551bacb7db3a24')

build() {
	export GOPATH="${srcdir}/godir"
	mkdir -p "$GOPATH"
	cd "${srcdir}/${pkgname}-${pkgver}"
	make
}

package() {
	cd "${srcdir}/${pkgname}-${pkgver}"
	install -D tir "${pkgdir}/usr/bin/tir"
}

