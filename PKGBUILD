pkgname=timeshift
pkgver=1.7.6
pkgrel=1
_ver=$pkgver'~184~ubuntu14.04.1'
pkgdesc='A system restore utility for Linux'
arch=('x86_64')
url='https://launchpad.net/timeshift'
license=('GPL')
depends=('gtk3' 'libsoup' 'desktop-file-utils' 'cronie' 'rsync' 'libgee' 'json-glib')
makedepends=('vala')
options=('!emptydirs')
source=("https://launchpad.net/~teejee2008/+archive/ubuntu/ppa/+files/${pkgname}_${_ver}.tar.gz")
sha256sums=('391b9716cd54060eb7f7b2058d9ca0486fcd41add4e5e44a568b27b94146e82e')

build() {
  cd $srcdir/$pkgname-$_ver
      make -s
}

package() {
  cd $srcdir/$pkgname-$_ver
  make DESTDIR="$pkgdir" install
  echo -en "#!/bin/bash\nkdesu timeshift" > $pkgdir/usr/bin/timeshift-launcher
}
