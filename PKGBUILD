# Maintainer: Diego <cdprincipe at gmail dot com>

pkgname=numix-icons-theme-git
pkgver=40.26473e0
pkgrel=1
pkgdesc="A dark icon theme for Numix Theme"
arch=('any')
url="https://github.com/cldx/numix"
license=('GPL3')
depends=()
makedepends=('git')
optdepends=()
provides=('icons-theme-numix')
conflicts=('icons-theme-numix')
source=('git://github.com/cldx/numix.git')
md5sums=('SKIP')

pkgver() {
  cd numix
  echo $(git rev-list --count HEAD).$(git rev-parse --short HEAD)
}

package() {
  cd numix

  # create theme dirs
  install -d -m 755 "$pkgdir"/usr/share/icons/Numix

  # clean up
  rm -rf {.git,.gitignore,CREDITS,LICENSE,README}

  # install theme
  cp -r . "$pkgdir"/usr/share/icons/Numix/

}

