# Maintainer: Jonas Heinrich <onny@project-insanity.org>
# Contributor: Jonas Heinrich <onny@project-insanity.org>

pkgname='perl-tftp'
pkgver='1.0b3'
pkgrel='2'
pkgdesc="TFTP - TFTP Client class for perl"
arch=('any')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl')
makedepends=()
url="http://search.cpan.org/~gsm/TFTP-${pkgver}/TFTP.pm"
source=("http://search.cpan.org/CPAN/authors/id/G/GS/GSM/TFTP-${pkgver}.tar.gz")
sha512sums=("45b117c55bd6f5954debcb35fd0250e6c002a119e3a44e68e529911db797882c35202b31c94e2aeea8e5400625eaf06f31a39122c30dffcc9e8a12919a4db32a")

build() {
    cd "${srcdir}/TFTP-${pkgver}"
    perl Makefile.PL INSTALLDIRS=vendor
    make
}

package(){
    cd "${srcdir}/TFTP-${pkgver}"
    make DESTDIR=$pkgdir install
}
