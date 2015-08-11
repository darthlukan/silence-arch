# Maintainer: Brian Tomlinson <darthlukan@gmail.com>
pkgname=openbox-theme-silence-arch-git
pkgver=1.0.8bf97ce
pkgrel=1
pkgdesc='A dark Openbox 3 theme'
arch=('any')
url='https://github.com/darthlukan/silence-arch'
license=('GPL2')

depends=('openbox')
makedepends=('git')
optdepends=()
provides=("${pkgname}-${pkgver}")
conflicts=("${pkgname}")

source=('silence-arch::git+https://github.com/darthlukan/silence-arch.git')
md5sums=('SKIP')

pkgver() {
   cd silence-arch
   printf "1.0.%s" "$(git rev-list --short HEAD)" 
}

package() {
    cd silence-arch
    rm -rf .git .gitignore README.md LICENSE
    mkdir -p ${pkgdir}/usr/share/themes/silence-arch
    cp -R * ${pkgdir}/usr/share/themes/silence-arch
}
