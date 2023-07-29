pkgname=mkinitcpio-ssh-encrypt
pkgver=1.0.0
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
  "c587712c7e7348b5d63b4bda67fadb220ed78e5a4d53015df37a779d27e8c03a"
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
