pkgname=mkinitcpio-ssh-encrypt
pkgver=1.0.1
pkgrel=1
pkgdesc="Enable remote unlock of an encrypted root device via SSH"
arch=("any")
url="https://github.com/kontextwechsel/arch-linux-ssh-encrypt.git"
license=("GPL")
source=(
  "hook"
  "install"
)
sha256sums=(
  "287c3ad612cfa25d71f431aae8f9bb54ef6825c0708121557018bc11fd2b1d91"
  "2544d85570e20324e4a394201cc880a898a00311d480c75c147724ff6787d157"
)

package() {
  depends=(
    "mkinitcpio"
    "dhclient"
    "dropbear"
  )
  install --owner=root --group=root --mode=644 -D "${srcdir}/hook" "${pkgdir}/usr/lib/initcpio/hooks/ssh-encrypt"
  install --owner=root --group=root --mode=644 -D "${srcdir}/install" "${pkgdir}/usr/lib/initcpio/install/ssh-encrypt"
}
