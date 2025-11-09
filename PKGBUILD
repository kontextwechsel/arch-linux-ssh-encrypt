pkgname=mkinitcpio-ssh-encrypt
pkgver=1.0.3
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
  "f743f1936f25d3a789cc1e2be96dab37239a83b7348f6e1e66348551944cac80"
  "fab9462bf292b7db4b7cf1df13ec5e6e4847b7f51b44e8abb582efb2e044a179"
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
