# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=haveged-s6serv
pkgver=0.1
pkgrel=2
pkgdesc="haveged service for s6"
arch=(x86_64)
license=('beerware')
depends=('haveged' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('haveged.daemon.run.s6'
		'haveged.log.run.s6'
		'haveged.logd'
		'LICENSE')
md5sums=('a78f18a9e2fed9f884c860dfe3186960'
         'ca718399a225d9c8c12456e5536622c4'
         'bb072ec1fb73112016f1db312556c93b'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/haveged.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/haveged/run"
	
	# log
	install -Dm 0755 "$srcdir/haveged.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/haveged/log/run"
	install -Dm 0644 "$srcdir/haveged.logd" "$pkgdir/etc/s6-serv/log.d/haveged"
	
	install -Dm 0755 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/haveged-s6serv/LICENSE"
}
