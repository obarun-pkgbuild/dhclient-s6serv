# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=dhclient-s6serv
pkgver=0.1
pkgrel=4
pkgdesc="dhclient service for s6"
arch=(x86_64)
license=('beerware')
depends=('dhclient' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('dhclient.daemon.run.s6'
		'dhclient.log.run.s6'
		'dhclient.logd'
		'LICENSE')
md5sums=('98eabe8cda59a249e69783319737d1b8'
         '88afa429987f01222006717423685394'
         '17fa0cbb35a1d02afc8d9d62c9e5c560'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/dhclient.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/dhclient/run"
	
	# log
	install -Dm 0755 "$srcdir/dhclient.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/dhclient/log/run"
	install -Dm 0644 "$srcdir/dhclient.logd" "$pkgdir/etc/s6-serv/log.d/dhclient"
	
	install -Dm 0755 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/dhclient-s6serv/LICENSE"
}
