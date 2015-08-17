# Maintainer: Francois Garillot <francois[@]garillot.net>
pkgname=r-cran-digest
pkgver=0.6.2
pkgrel=1
pkgdesc="Create cryptographic hash digests of R objects"
url="http://cran.r-project.org/web/packages/digest/index.html"
license=('GPL-2')
arch=('i686' 'x86_64')
makedepends=('gcc' 'gcc-fortran')
depends=('r' )
optdepends=()
source=(http://cran.r-project.org/src/contrib/digest_$pkgver.tar.gz)
build() {
    mkdir -p ${pkgdir}/usr/lib/R/library
    cd ${srcdir}
    R CMD INSTALL digest -l ${pkgdir}/usr/lib/R/library
    for lic in "LICENSE" "LICENCE" "COPYING"; do
        if [ -f ${srcdir}/digest/${lic} ]; then
            install -Dm644 ${srcdir}/digest/${lic} ${pkgdir}/usr/share/licenses/r-cran-digest/${lic}
        fi
    done
}
md5sums=('8d02d3581e4df0f8020bfce6c23cf3e4')
