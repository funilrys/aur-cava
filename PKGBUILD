# Maintainer: Nissar Chababy <funilrys at outlook dot com>
# Ex-Maintainer: Celestial Walrus <aur@celestial.cf>

pkgname=cava
pkgver=0.10.3
pkgrel=2
pkgdesc='Console-based Audio Visualizer for Alsa'
arch=('any')
url='https://github.com/karlstav/cava'
license=('MIT')
depends=('fftw' 'alsa-lib' 'ncurses' 'iniparser' 'sndio' 'portaudio')
optdepends=('pulseaudio' 'pipewire')
makedepends=('sndio' 'portaudio' 'libpulse' 'm4' 'automake' 'autoconf' 'libpipewire')
source=("$pkgname-$pkgver.tar.gz::https://github.com/karlstav/cava/releases/download/0.10.3/${pkgname}-${pkgver}.tar.gz")
sha512sums=('15fa550da266d3d4b917da0e6b5611bd7b82e5d30d15e3d728b0e3d5a92387787156e3e32f632f68b9c5e217a023bc2b3ca4ffd48ac6e03be1519ec2b504b13a')

build() {
  cd ${pkgname}-${pkgver}
  ./configure --prefix=/usr
  make
}

package() {
  cd ${pkgname}-${pkgver}
  install -Dm755 cava "$pkgdir/usr/bin/cava"
  install -Dm644 LICENSE "$pkgdir"/usr/share/licenses/"${pkgname}"/LICENSE
}
