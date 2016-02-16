# Maintainer: Michael Herold <arch@michaeljherold.com>
# Maintainer: Ainola

pkgname=scudcloud
pkgver=1.15
pkgrel=1
pkgdesc="A Linux client for Slack"
arch=('any')
url="https://github.com/raelgc/scudcloud"
license=('MIT')
depends=('python-dbus' 'python-pyqt4')
makedepends=('python-setuptools')
install=${pkgname}.install
source=("$pkgname-$pkgver.tar.gz::https://github.com/raelgc/scudcloud/archive/v${pkgver}.tar.gz")
sha256sums=('76290173588e7eb2c8308a804536861d4a5e7660428fd538ccc167fd6a47612b')

package() {
    cd "$pkgname-$pkgver"
    python setup.py install --prefix=/usr --root="$pkgdir"
    rm -rf "$pkgdir/usr/share/icons/ubuntu"*

    # license
    install -dm755 "$pkgdir/usr/share/licenses/$pkgname"
    install -Dm644 "$pkgdir/usr/share/doc/$pkgname/LICENSE" \
        "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
