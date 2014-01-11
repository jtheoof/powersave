# Maintainer: Jeremy Attali <jeremy.attali@gmail.com>

pkgname=jtheoof-powersave-git
pkgver=0.2.2
pkgrel=1
pkgdesc="Arch Linux Powersave package for Dell Inspiron 7000 (7537)"

arch=('any')
url="http://github.com/jtheoof/powersave"
license=('MIT')
depends=('systemd' 'ethtool' 'rfkill')
makedepends=('git')
source=("git+file://$PWD")
sha1sums=('SKIP')

package() {
  cd "powersave"
  install -Dm755 bin/powersave "$pkgdir/usr/local/bin/powersave"
  install -Dm644 modprobe.d/i915.conf "$pkgdir/etc/modprobe.d/i915.conf"
  install -Dm644 rules.d/50-powersave.rules "$pkgdir/etc/udev/rules.d/50-powersave.rules"
  install -Dm644 rules.d/50-powersave-pci.rules "$pkgdir/etc/udev/rules.d/50-powersave-pci.rules"
  install -Dm644 rules.d/50-powersave-usb.rules "$pkgdir/etc/udev/rules.d/50-powersave-usb.rules"
  install -Dm644 systemd/powersave.service "$pkgdir/usr/lib/systemd/system/powersave.service"
  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

# vim: ft=sh syn=sh sts=2 sw=2 et tw=0
