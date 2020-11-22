## Maintainer: David Husička <contact@bydave.net>

pkgname=osu-lazer-bin
pkgver=2020.1121.0
pkgrel=1
pkgdesc="The future of osu! and the beginning of an open era! Commonly known by the codename osu!lazer. Pew pew."
arch=('x86_64')
url="https://osu.ppy.sh"
license=('MIT' 'custom:CC-BY-NC 4.0')
groups=()
depends=(ffmpeg zlib)
makedepends=()
checkdepends=()
optdepends=()
provides=(osu osu-lazer)
conflicts=(osu osu-lazer)
replaces=()
backup=()
options=(!strip)
install=
changelog=
source=("$pkgname-$pkgver.AppImage::https://github.com/ppy/osu/releases/download/$pkgver/osu.AppImage"
        "$pkgname.png::https://raw.githubusercontent.com/ppy/osu/master/assets/lazer.png"
        "$pkgname-LICENCE.md::https://raw.githubusercontent.com/ppy/osu-resources/master/LICENCE.md"
        "osu-lazer.desktop")
noextract=("$pkgname-$pkgver.AppImage")
sha256sums=("df1f732178073fa45516e7957a25f377c9ce7a933e49b9a9ac8586a3d989fdf2"
            "36f73cfe0a84cd65a8bb54fcde5a01c419b134bee4a88cc92eb4f33236343a10"
            "30b914824784b6ba6b30a44b22bea4f3c6fbc10f3f0e74fde5ca76a92ef57244"
            "f37168074db22cf8e898f08b3f67458e1708a8c4ae179fb14a916e74e12bec4e")

package() {
	 # Install image
	 install -Dm644 "${srcdir}"/"${pkgname}".png "${pkgdir}"/usr/share/pixmaps/osu-lazer.png

	 # Install license
	 install -Dm644 "${srcdir}"/"${pkgname}"-LICENCE.md "${pkgdir}"/usr/share/licenses/"${pkgname}"/LICENCE.md

	 # Install desktop file
	 install -Dm644 osu-lazer.desktop "${pkgdir}"/usr/share/applications/osu-lazer.desktop

	 # Install binary
	 install -Dm755 "${srcdir}"/"${pkgname}"-"${pkgver}".AppImage "${pkgdir}"/usr/bin/osu

}
