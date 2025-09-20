pkgname=mkinitcpio-ssh-encrypt
pkgver=1.0.2
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
  "a57e476cc36190b1b974c24c9044bd835fda6043320df8e9cf45a55e5b26b8af"
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
