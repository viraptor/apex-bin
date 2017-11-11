# $Id$
# Maintainer: Ido Kanner <idokan@gmail.com>
pkgname=apex-bin
_pkgname=apex
pkgdesc="Build, deploy, and manage AWS Lambda functions with ease (with Go support!)."
pkgver=0.16.0
pkgrel=2
arch=('i686' 'x86_64')
license=('MIT')
url='http://apex.run/'
provides=('apex' 'apex.run')
noextract=()
makedepends=('binutils')
_local_name="${_pkgname}_${CARCH}_${pkgver}"
source_i686=("${_local_name}::https://github.com/apex/apex/releases/download/v${pkgver}/${_pkgname}_linux_386")
source_x86_64=("${_local_name}::https://github.com/apex/apex/releases/download/v${pkgver}/${_pkgname}_linux_amd64")
sha256sums_i686=('82458e688d724349408d451ebfa25a7025284112264f2be6206091a9c0c1f58d')
sha256sums_x86_64=('ad1f4f8cb5577aeff84fd5edf7234fe45178811022e020cec1ae9c72ee46f79c')

prepare() {
  mv "${_local_name}" "$_pkgname"
  strip "$_pkgname"
}

package() {
  mkdir -p "$pkgdir"/usr/bin
  install -Dm0755 "$_pkgname" "$pkgdir"/usr/bin
}
