# Contributor: paul2lv [at] gmail dot com
# Maintainer: 

pkgname=fahviewer-beta-bin
pkgver=7.4.16
pkgrel=1
pkgdesc="A Folding@home 3D simulation viewer"
url="http://folding.stanford.edu/English/HomePage"
arch=('x86_64')
license=('GPL2')
depends=('glew' 'gtk2' 'freetype2' 'glut')
conflicts=('fahviewer')
replaces=('fahviewer')
options=('!docs' '!libtool')
source=('https://folding.stanford.edu/releases/beta/release/fahviewer/debian-stable-64bit/v7.4/fahviewer_7.4.16-64bit-release.tar.bz2')
sha256sums=('56bdc4f64451f5c1dc43cbc2332e044b7b4c2f3bd41b26f25b7c69b2a529ab1c')


package() {
	cd ${srcdir}
	install -dm755 ${pkgdir}/opt/fah-beta/
	cp -rf fahviewer_${pkgver}-64bit-release/backgrounds ${pkgdir}/opt/fah-beta/

	install -d "${pkgdir}/usr/bin"
	install -D -m0755 ${srcdir}/fahviewer_${pkgver}-64bit-release/FAHViewer ${pkgdir}/opt/fah-beta/FAHViewer
	ln -s "/opt/fah-beta/FAHViewer" "${pkgdir}/usr/bin/FAHViewer"
}
