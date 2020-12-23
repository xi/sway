pkgname=$(basename $(pwd))-deps
pkgdesc='i3-compatible wayland compositor'
pkgver=$(git describe --always | sed 's/^v//')
arch=('amd64')
url=$(git remote get-url origin)
depends=(
	'meson(>=0.53.1)'
	build-essential
	cmake

	xwayland
	libpcre3-dev
	libpango1.0-dev
	libcairo2-dev
	libgdk-pixbuf2.0-dev
	'scdoc(>=1.9.2)'

	# wlroots
	libwayland-dev
	wayland-protocols
	libegl1-mesa-dev
	libgles2-mesa-dev
	libdrm-dev
	libgbm-dev
	libinput-dev
	libxkbcommon-dev
	libudev-dev
	libpixman-1-dev
	libsystemd-dev
	libxcb1-dev
	libxcb-composite0-dev
	libxcb-xfixes0-dev
	libxcb-xinput-dev
	libxcb-image0-dev
	libxcb-render-util0-dev
	libx11-xcb-dev
	libxcb-icccm4-dev
	freerdp2-dev
	libwinpr2-dev
	libpng-dev
	libavutil-dev
	libavcodec-dev
	libavformat-dev
)
