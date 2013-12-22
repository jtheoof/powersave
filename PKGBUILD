# Maintainer: Jeremy Attali <jeremy.attali@gmail.com>

pkgname=jtheoof-powersave-git
pkgver=1
pkgver() {
  cd "powersave"
  git describe | sed 's/^v//;s/-/./g'
}
pkgrel=1
pkgdesc="Arch Linux Powersave package for Dell Inspiron 7000 (7537)"

arch=('any')
url="http://github.com/jtheoof/powersave"
license=('MIT')
depends=('systemd')
makedepends=('git')
source=("git+file://$PWD")
sha1sums=('SKIP')

package() {
  cd "powersave"
  install -Dm755 bin/powersave "$pkgdir/usr/local/bin/powersave"
  install -Dm644 rules.d/50-powersave.rules "$pkgdir/etc/udev/rules.d/50-powersave.rules"
}

# vim: ft=sh syn=sh sts=2 sw=2 et
