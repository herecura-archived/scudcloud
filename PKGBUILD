# Maintainer: Michael Herold <arch@michaeljherold.com>
# Maintainer: Ainola

pkgname=scudcloud
pkgver=1.28
pkgrel=1
pkgdesc="A Linux client for Slack"
arch=('any')
url="https://github.com/raelgc/scudcloud"
license=('MIT')
depends=('python-dbus' 'python-pyqt4' 'desktop-file-utils' 'hicolor-icon-theme')
makedepends=('python-setuptools')
source=("$pkgname-$pkgver.tar.gz::https://github.com/raelgc/scudcloud/archive/v${pkgver}.tar.gz")
sha256sums=('5eff701fe9e593101ddcc96f79de8d19ddde0227a0905e5dcc39ff96fc03666e')

package() {
    cd "$pkgname-$pkgver"
    python setup.py install --prefix=/usr --root="$pkgdir"
    rm -rf "$pkgdir/usr/share/icons/ubuntu"*

    # license
    install -dm755 "$pkgdir/usr/share/licenses/$pkgname"
    install -Dm644 "$pkgdir/usr/share/doc/$pkgname/LICENSE" \
        "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
