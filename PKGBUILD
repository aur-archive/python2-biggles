# Contributor: Cesar G. Miguel <cesargm@lsi.usp.br>, Mathieu Westphal <mathieu.westphal@gmail.com>
pkgname=python2-biggles
pkgver=1.6.6
pkgrel=3
pkgdesc="Scientific Plotting for Python"
arch=('any')
url="http://biggles.sourceforge.net/"
license=('GPL')
depends=('python2>=1.5.2' 'plotutils>=2.4.1' 'python2-numpy')
source=("http://downloads.sourceforge.net/sourceforge/biggles/$pkgname-$pkgver.tar.gz")
md5sums=('5a9cfdf9d8401e1705fce43e4e4adaca')

build() {
    cd "$srcdir/$pkgname-$pkgver"
    python2 setup.py build_ext -I /usr/lib/
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  mkdir -p "$pkgdir/usr/"
  python2 setup.py install --prefix "$pkgdir/usr/"
}

