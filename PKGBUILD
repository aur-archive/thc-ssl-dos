# Maintainer: Testuser_01 <arch@nico-siebler.de>

pkgname=thc-ssl-dos
pkgver=1.4
pkgrel=2
pkgdesc="THC-SSL-DOS is a tool to verify the performance of SSL. To be used in your authorized and legitimate area ONLY. You need to accept this to make use of it, no use for bad intentions, you have been warned!"
url="http://www.thc.org/${pkgname}/"
arch=('any')
install="${pkgname}.install"
license=('custom: unknown')
depends=('openssl' 'glibc' 'zlib')
source=("http://www.thc.org/${pkgname}/${pkgname}-${pkgver}.tar.gz")
md5sums=('0d75fc5d6aaf22130c57436fea3ca339')

build() {
	cd "${srcdir}/${pkgname}-${pkgver}" || return 1
	./configure --prefix=/usr || return 1
	make all || return 1
	mkdir -p "${pkgdir}/usr/bin/" || return 1
	install -m755 -D "src/${pkgname}" "${pkgdir}/usr/bin/" || return 1
	msg "---"
	msg "THC-SSL-DOS is a tool to verify the performance of SSL. To be used in your authorized and legitimate area ONLY. You need to accept this to make use of it, no use for bad intentions, you have been warned!"
	msg "---"
}
