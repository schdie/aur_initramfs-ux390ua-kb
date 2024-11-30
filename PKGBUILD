# Maintainer: none

pkgname=initramfs-ux390ua-kb
pkgdesc="initramfs hook to turn the ASUS ux390 keyboard backlight on at boot."
pkgver=1.0
pkgrel=3
license=(MIT)
arch=(any)
depends=(mkinitcpio)
source=('ux390ua.hook'
				'ux390ua.install'
				'README.md')

build() {
	return 0
}

package() {
	mkdir -p "${pkgdir}/usr/lib/initcpio/hooks"
	mkdir -p "${pkgdir}/usr/lib/initcpio/install"

	cp "${srcdir}/ux390ua.hook" "${pkgdir}/usr/lib/initcpio/hooks/ux390ua_kb_backlight"
	cp "${srcdir}/ux390ua.install" "${pkgdir}/usr/lib/initcpio/install/ux390ua_kb_backlight"

	mkdir -p "${pkgdir}/usr/share/doc/${pkgname}"
	cp "${srcdir}/README.md" "${pkgdir}/usr/share/doc/${pkgname}/"
}

sha256sums=('53879a9290d324439f4bd37c5d12ddeca8371c2eca12a5b5e897d961c8798571'
            'ddb45cc3358aa58a45b86ec3f1c88cc80c46cf32fed349c22fff22f8e8339dd6'
            '3733816f214ee4926e634304d5c5dbcd40aba937ba0a715e642c223ec43ceb8b')
