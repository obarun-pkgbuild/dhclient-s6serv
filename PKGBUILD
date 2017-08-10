# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=dhclient-s6serv
pkgver=0.1
pkgrel=2
pkgdesc="dhclient service for s6"
arch=(x86_64)
license=('beerware')
depends=('dhclient' 's6' 's6-rc' 's6-boot')
conflicts=()
install=dhclient-s6serv.install
source=('dhclient.daemon.run.s6'
		'dhclient.log.run.s6'
		'LICENSE')
md5sums=('98eabe8cda59a249e69783319737d1b8'
         '88afa429987f01222006717423685394'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/dhclient.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/dhclient/run"
	
	# log
	install -Dm 0755 "$srcdir/dhclient.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/dhclient/log/run"
	
	install -Dm 0755 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/dhclient-s6serv/LICENSE"
}
