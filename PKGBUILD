# Contributor: SubNeX
# Contributor: Estuera (Modified to i386)

pkgname=scangearmp-i386
pkgver=1.60
pkgrel=1
pkgdesc="Canon IJ Scanner Driver (Common package) i386"
url="http://www.canon.dk/Support/Consumer_Products/products/Fax__Multifunctionals/InkJet/PIXMA_MP_series/MP495.aspx?type=download&page=1"
arch=('i386')
arch=('i686')
license=('custom')
depends=('sane' 'gtk2>=2.4.0' 'gimp>=2.0.0' 'libpng>=1.2.8' 'libusb>=0.1.12')
conflicts=('scangearmp')
makedepends=('rpmextract')
source=(http://files.canon-europe.com/files/soft40270/Software/MP495series-scanner_driver.tar)
md5sums=('9217ca25d62677ce2b24d0e95da35f4c')

build() {
  cd $startdir/pkg/
  tar -xvf $startdir/MP495series-scanner_driver.tar 
  tar -xvf $startdir/src/scangearmp-mp495series-$pkgver-1-rpm.tar.gz scangearmp-mp495series-$pkgver-1-rpm/packages/scangearmp-common-$pkgver-1.i386.rpm


  rpmextract.sh $startdir/pkg/scangearmp-mp495series-$pkgver-1-rpm/packages/scangearmp-common-$pkgver-1.i386.rpm
#  mkdir -p usr/share/licenses/${pkgname}
#  cp -r usr/share/doc/cnijfilter-common-$pkgver/* usr/share/licenses/${pkgname}
  chmod -R a+rX usr/
}
