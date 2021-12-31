# Maintainer: BadBoy <luckmelove2@gmail.com>

pkgname='oxygen-cursors'
pkgver='1.0.0'
pkgrel='1'
pkgdesc='Made by LHt Cursors themes'
arch=('any')
license=('GPL3')
depends=('lxappearance' 'libx11' 'libxcursor' 'libpng')
source=('oxygen-cursors.tar.bz2'
)

sha256sums=('SKIP'
)

package() {
    msg 'This Private cursors themes'
    for i in "${pkgname}"/*
    do
        page=$(echo ${i}|cut -d '/' -f '2')
        install -dm755 "${i}" "${pkgdir}"/usr/share/icons/"${page}"/cursors

        install -Dm644 "${srcdir}/${i}"/*theme "${pkgdir}"/usr/share/icons/"${page}"
        install -Dm644 "${srcdir}/${i}"/cursors/* "${pkgdir}"/usr/share/icons/"${page}"/cursors
    done
}
