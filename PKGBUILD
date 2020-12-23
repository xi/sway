pkgname=$(basename $(pwd))
pkgdesc='i3-compatible wayland compositor'
pkgver=$(git describe --always)
arch=('amd64')
url=$(git remote get-url origin)
depends=(libpcre3 libjson-c3 libpango-1.0-0 libcairo2)
provides=(wlroots swaybg)
conflicts=(wlroots swaybg)
# MESON_OPTS='--reconfigure'

package() {
	meson --prefix="/usr" $MESON_OPTS build
	DESTDIR="$pkgdir" ninja -C build install

	cd subprojects
	if [ ! -d swaybg ]; then
		git clone https://github.com/swaywm/swaybg.git
	fi
	cd swaybg
	meson --prefix="/usr" $MESON_OPTS build
	DESTDIR="$pkgdir" ninja -C build install
}
