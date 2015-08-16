#Maintainer: Nitin Mathew <nitn_mathew2000@hotmail.com>                                                                                             
#Contributor: Nitin Mathew <nitn_mathew2000@hotmail.com>                                                                                                                                                                                                                              
pkgname=idrive-wrapper                                                                                                                               
pkgver=1.2
pkgrel=1
pkgdesc="Wrapper for idevsutil utility from IDrive for online backup"                                        
arch=('x86_64')
url="https://github.com/nsmathew/idrive-wrapper"
license=('GPL3')
depends=('idevsutil')
install=$pkgname.install
source=(https://github.com/nsmathew/idrive-wrapper/archive/v${pkgver}.tar.gz ${pkgname}.install)
sha256sums=('98e2bab01ae82939e4fbfda161b1166e7ee6a445d762979d565fc721d0cca929' 'b67938d185f6b2684e471dc70d788852fca269533c126a0dc9e1f0c66707eba3')

package() {
        cd ${srcdir}/${pkgname}-${pkgver}
        install -D -m755 idrive-wrapper.sh ${pkgdir}/usr/bin/idrive-wrapper
        install -D -m644 COPYING ${pkgdir}/usr/share/licenses/idrive-wrapper/COPYING
        install -D -m644 .idrivewrc ${pkgdir}/usr/share/doc/idrive-wrapper/.idrivewrc
        install -D -m644 idrive-wrapper_manual.txt ${pkgdir}/usr/share/doc/idrive-wrapper/idrive-wrapper_manual.txt

	#Remove the downloaded source
	cd ../.. && rm -fr v${pkgver}.tar.gz
}
