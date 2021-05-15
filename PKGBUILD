# Maintainer: Ashin Antony <ashinant15@gmail.com>

pkgname=tabbed-ashin-git
pkgver=0.6
pkgrel=1
pkgdesc='A suckless tab utility customized in my own way with hidetabs and icons.'
arch=(x86_64 i686)
url='https://github.com/ashincoder/tabbed-ashin.git'
license=('MIT')
depends=(libxrandr)
optdepends=('surf: suckless browser'
            'st: simple terminal')
makedepends=(git) 
checkdepends=()
provides=(tabbed)
conflicts=(tabbed)
replaces=()
backup=()
options=()
source=("git+$url")
noextract=()
md5sums=('SKIP')
validpgpkeys=()

pkgver() {
  cd tabbed-ashin
  printf "0.6.r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

build() {
  cd tabbed-ashin
  make PREFIX=/usr 
}

package() {
  cd tabbed-ashin  
  mkdir -p ${pkgdir}/opt/${pkgname}
  cp -rf * ${pkgdir}/opt/${pkgname}
  make PREFIX=/usr DESTDIR="${pkgdir}" install
  install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
  install -Dm644 README.md "${pkgdir}/usr/share/doc/${pkgname}/README.md"
}

