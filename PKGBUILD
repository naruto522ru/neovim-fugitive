# Maintainer: Levente Polyak <anthraxx[at]archlinux[dot]org>
# Contributor: Daniel Micay <danielmicay@gmail.com>
# Contributor: M Rawash <mrawash@gmail.com>
# Contributor: János Illés <ijanos@gmail.com>
_pkgname=vim-fugitive
pkgname=neovim-fugitive
pkgver=3.2
pkgrel=1
pkgdesc='Git wrapper so awesome, it should be illegal'
url='https://github.com/tpope/vim-fugitive'
arch=('any')
license=('custom:vim')
depends=('git')
#groups=('vim-plugins')
source=("${url}/archive/v${pkgver}/${_pkgname}-${pkgver}.tar.gz"
        license.txt)
sha512sums=('c7ac97d52f683a73545efddf33986dedecbae25208ebf0703dccf99cb46fd5020362f724c5b530aeca40467d9e864ce6597d6eb5eaa93a33643191e1aa5b44db'
            'a50e91b1896b0d952008ba2f641a87af2d1a01e4f280f6c914edcd51ae5d1586d5ade71c3609866b501569007bcb7f2494f08280afec170884b90fab36332fac')
b2sums=('cab484ec66b7c54857856ed1f6cbebbf6d3fb1afdb35b004f72f8c06785a18d8810244255305cd949e25d1f78d734c46e400488526631b4070d3e0b104830552'
        '63a85fc6710dc62cf9d982eaf8fa048ccc81754e9c67c6a071ae9608c7ba90f07d744733f377e08078612dcc9a0e33590c96f4a4a1f81cdba72f86bddf34e324')

package() {
  cd ${_pkgname}-${pkgver}
  local _installpath="${pkgdir}/usr/share/nvim/runtime"
  install -d "${_installpath}"
  cp -r -t "${_installpath}" autoload doc plugin ftdetect syntax
  mv "${pkgdir}/usr/share/nvim/runtime/ftdetect" "${pkgdir}/usr/share/nvim/runtime/ftplugin"

  install -Dm 644 ../license.txt -t "${pkgdir}/usr/share/licenses/${pkgname}"
}

# vim: ts=2 sw=2 et:
