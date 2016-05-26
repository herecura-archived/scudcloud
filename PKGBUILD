# Maintainer: Michael Herold <arch@michaeljherold.com>
# Maintainer: Ainola

pkgname=scudcloud
pkgver=1.24
pkgrel=1
pkgdesc="A Linux client for Slack"
arch=('any')
url="https://github.com/raelgc/scudcloud"
license=('MIT')
depends=('python-dbus' 'python-pyqt4' 'desktop-file-utils' 'hicolor-icon-theme')
makedepends=('python-setuptools')
source=("$pkgname-$pkgver.tar.gz::https://github.com/raelgc/scudcloud/archive/v${pkgver}.tar.gz")
sha256sums=('75a035d920b305720e2723146a92444eb087ef6420b0140c415962e73234927d')

package() {
    cd "$pkgname-$pkgver"
    python setup.py install --prefix=/usr --root="$pkgdir"
    rm -rf "$pkgdir/usr/share/icons/ubuntu"*

    # license
    install -dm755 "$pkgdir/usr/share/licenses/$pkgname"
    install -Dm644 "$pkgdir/usr/share/doc/$pkgname/LICENSE" \
        "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
