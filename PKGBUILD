# Maintainer:  Hyacinthe Cartiaux <hyacinthe.cartiaux at free.fr>
# Contributor: Arkham <arkham at archlinux dot us>
# Contributor: StaCk <proc.null at gmail dot com>

pkgname=fhs-manpages
pkgver=2.2
pkgrel=1
pkgdesc="A manpage for the Filesystem Hierarchy Standard."
arch=('any')
depends=('gzip')
url="http://github.com/alyptik/fhs-manpages"
license=('GPL')
source=("https://github.com/alyptik/${pkgname}/raw/master/fhs.mm")
sha256sums=('78151512ca871eea57bd76daddf6768ec2fa6a847f33b6333f6411a1dd1074a3')
build() {
	cat "$srcdir/fhs.mm" | gzip > "$srcdir/fhs.5.gz"
}
package() {
    install -d "$pkgdir/usr/share/man/man5/"
    install -m 644 "$srcdir/fhs.5.gz" "$pkgdir/usr/share/man/man5/"
}
