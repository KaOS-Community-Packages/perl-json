# $Id: PKGBUILD 100320 2013-11-02 09:14:26Z spupykin $

pkgname=perl-json
pkgver=2.90
pkgrel=1
pkgdesc="JSON (JavaScript Object Notation) encoder/decoder"
arch=('x86_64')
url="http://search.cpan.org/dist/JSON"
license=('GPL' 'PerlArtistic')
depends=('perl>=5.10.0')
options=('!emptydirs')
source=(http://www.cpan.org/authors/id/M/MA/MAKAMAKA/JSON-$pkgver.tar.gz)
md5sums=('e1512169a623e790a3f69b599cc1d3b9')

build() {
  cd  $srcdir/JSON-$pkgver
  PERL_MM_USE_DEFAULT=1 perl Makefile.PL INSTALLDIRS=vendor
  make
}

package() {
  cd  $srcdir/JSON-$pkgver
  make install DESTDIR=$pkgdir
  find $pkgdir -name '.packlist' -delete
  find $pkgdir -name '*.pod' -delete
}
