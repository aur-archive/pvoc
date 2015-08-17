# Maintainer: SpepS <dreamspepser at yahoo dot it>

pkgname=pvoc
pkgver=0.1.12
pkgrel=1
pkgdesc="LADSPLA plugins and a tool for time compression/expansion using phase-vocoding"
arch=(i686 x86_64)
url="http://quitte.de/dsp/pvoc.html"
license=('GPL')
groups=('ladspa-plugins')
depends=('fftw' 'libsndfile')
makedepends=('ladspa')
optdepends=('ladspa: plugins')
source=("http://quitte.de/dsp/${pkgname}_$pkgver.tar.gz")
md5sums=('6171b97e0d8aa5545c780d4f8dc15167')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  make PREFIX=/usr
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make PREFIX="$pkgdir/usr" \
       MAN1DEST="$pkgdir/usr/share/man/man1" install
}

# vim:set ts=2 sw=2 et:
