# Contributor: Martin Lefebvre <dadexter@gmail.com>

pkgname=pebrot
pkgver=0.8.9
pkgrel=4
pkgdesc="Pebrot is a text MSN messenger client implemented with Python."
arch=('any')
url="http://pebrot.sourceforge.net/"
license=('GPL')
depends=('python2')
source=(http://downloads.sourceforge.net/sourceforge/${pkgname}/${pkgname}-${pkgver}.tar.gz)
md5sums=('a091be98cebde3de00c3dc23df066bac')

build() {
  cd ${srcdir}/${pkgname}-${pkgver}
  sed -i 's#env python#env python2#' utils/{*.py,transparent_bg/setup.py}
  python2 setup.py install --root=${pkgdir} || return 1
  install -D -m644 pebrotrc ${pkgdir}/etc/pebrotrc
  install -d ${pkgdir}/usr/share/pebrot
  install -m644 logos/*.txt ${pkgdir}/usr/share/pebrot/
}
