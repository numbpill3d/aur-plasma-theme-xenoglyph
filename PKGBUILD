# Maintainer: numbpill3d <void@nothing>
# Contributor: numbpill3d <void@nothing>
pkgname=plasma-theme-xenoglyph
pkgname+=(sddm-theme-xenoglyph)
pkgname+=(plymouth-theme-xenoglyph)
pkgver=1.0
pkgrel=1
pkgdesc='Alien-white cybertribal KDE Plasma 6 theme suite by splicer scorn (voidrane)'
arch=('any')
url='https://github.com/numbpill3d/xenoglyph'
license=('GPL-3.0-or-later')
depends=('plasma-workspace' 'kwin' 'kvantum' 'kde-icon-theme')
optdepends=(
  'konsole: Konsole terminal colour scheme'
  'kitty: kitty terminal colour scheme'
  'sddm: SDDM login theme'
  'plymouth: Plymouth boot splash'
)
source=("${pkgname}-1.0.tar.gz::https://github.com/numbpill3d/xenoglyph/archive/refs/tags/v1.0.tar.gz")
sha256sums=('SKIP')


package_plasma-theme-xenoglyph() {
  cd "$srcdir/xenoglyph-1.0"

  install -d "$pkgdir/usr/share/plasma/desktoptheme"
  cp -r plasma/desktoptheme/Xenoglyph "$pkgdir/usr/share/plasma/desktoptheme/"
  install -d "$pkgdir/usr/share/plasma/look-and-feel"
  cp -r plasma/look-and-feel/scorn.xenoglyph "$pkgdir/usr/share/plasma/look-and-feel/"
  install -d "$pkgdir/usr/share/plasma/plasmoids"
  cp -r plasma/plasmoids/scorn.xenoglyph.sigil "$pkgdir/usr/share/plasma/plasmoids/"
  install -d "$pkgdir/usr/share/plasma/wallpapers"
  cp -r plasma/wallpapers/scorn.xenoglyph "$pkgdir/usr/share/plasma/wallpapers/"
  install -d "$pkgdir/usr/share/plasma/wallpapers"
  cp -r plasma/image-wallpaper/Xenoglyph "$pkgdir/usr/share/plasma/wallpapers/"
  install -d "$pkgdir/usr/share/aurorae/themes"
  cp -r aurorae/Xenoglyph "$pkgdir/usr/share/aurorae/themes/"
  install -Dm644 colors/Xenoglyph.colors "$pkgdir/usr/share/color-schemes/Xenoglyph.colors"
  install -d "$pkgdir/usr/share/icons"
  cp -r icons/Xenoglyph "$pkgdir/usr/share/icons/"
  install -d "$pkgdir/usr/share/Kvantum"
  cp -r kvantum/Xenoglyph "$pkgdir/usr/share/Kvantum/"
  install -d "$pkgdir/usr/share/kwin/effects"
  cp -r kwin/xenoglyph_runes kwin/xenoglyph_unfurl "$pkgdir/usr/share/kwin/effects/"
  install -Dm644 terminal/Xenoglyph.colorscheme "$pkgdir/usr/share/konsole/Xenoglyph.colorscheme"
  install -Dm644 terminal/Xenoglyph.profile "$pkgdir/usr/share/konsole/Xenoglyph.profile"
  install -Dm644 terminal/xenoglyph-kitty.conf "$pkgdir/usr/share/kitty/themes/xenoglyph-kitty.conf"

  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

package_sddm-theme-xenoglyph() {
  depends=('sddm')
  optdepends=('plasma-theme-xenoglyph: the Plasma 6 half of the suite')
  pkgdesc='SDDM login theme — Alien-white cybertribal KDE Plasma 6 theme suite by splicer scorn (voidrane)'
  cd "$srcdir/xenoglyph-1.0"
  install -d "$pkgdir/usr/share/sddm/themes"
  cp -r sddm/xenoglyph "$pkgdir/usr/share/sddm/themes/"
  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

package_plymouth-theme-xenoglyph() {
  depends=('plymouth')
  optdepends=('plasma-theme-xenoglyph: the Plasma 6 half of the suite')
  pkgdesc='Plymouth boot splash — Alien-white cybertribal KDE Plasma 6 theme suite by splicer scorn (voidrane)'
  cd "$srcdir/xenoglyph-1.0"
  install -d "$pkgdir/usr/share/plymouth/themes"
  cp -r plymouth/xenoglyph "$pkgdir/usr/share/plymouth/themes/"
  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
