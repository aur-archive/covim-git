# Maintainer: Nicolas Cornu <ncornu@aldebaran-robotics.com>

pkgname=covim-git
_gitname=covim
pkgver=75.37f1766
pkgrel=1
pkgdesc="CoVim plugin for Vim"
arch=('any')
url="https://github.com/FredKSchott/CoVim"
depends=('gvim')
makedepends=('git')
provides=('covim')
license=('custom')
source=(${_gitname}::git+https://github.com/FredKSchott/CoVim.git)
sha256sums=('SKIP')

pkgver() {
  cd ${_gitname}
  echo $(git rev-list --count HEAD).$(git rev-parse --short HEAD)
}

package() {
  cd ${_gitname}
  install -dm 755 "${pkgdir}"/usr/share/vim/vim73/{plugin,doc}
  install -m 644 plugin/* "${pkgdir}"/usr/share/vim/vim73/plugin
  install -m 644 doc/* "${pkgdir}"/usr/share/vim/vim73/doc
  install -Dm 644 LICENCE "${pkgdir}"/usr/share/licenses/${_gitname}/LICENCE
}
