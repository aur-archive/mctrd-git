# Maintainer: Kurashov Artem Konstantinovich <mail@saahriktu.org>
# Contributor: Ivan Shapovalov <intelfx100@gmail.com>

pkgname=mctrd-git
pkgver=r19.41ea56a
pkgrel=1
pkgdesc="Command line tool for add/extract files from .scl and .trd images"
arch=('i686' 'x86_64')
url="https://github.com/samstyle/mctrd"
source=('git://github.com/samstyle/mctrd')
sha1sums=('SKIP')

pkgver() {
  cd mctrd
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

build() {
  cd mctrd
  make
}

package() {
  cd mctrd
  install -Dm755 mctrd "$pkgdir/usr/bin/mctrd"
}
