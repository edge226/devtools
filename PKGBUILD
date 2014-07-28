# Maintainer: Edward Tunnah <edge226@dem0n.com>
# Contributors: Lane Wiscombe <anex@dem0n.com>

pkgname=devtools-openrc
pkgver=20140728
pkgrel=1
pkgdesc='Packaging Tools For Lucid Systems'
arch=('any')
license=('GPL')
url='http://git.manjaro.org/core/devtools/'
depends=('namcap' 'openssh' 'subversion' 'rsync' 'arch-install-scripts')
conflicts=('devtools-systemd' 'devtools')
source=('https://github.com/edge226/devtools/archive/openrc.zip')
sha256sums=('SKIP')

build() {
	cd "$pkgname"
	make PREFIX=/usr
}

package() {
	rm -rf /var/lib/manjarobuild/*
	cd "$pkgname"
	make PREFIX=/usr DESTDIR=${pkgdir} install
}
