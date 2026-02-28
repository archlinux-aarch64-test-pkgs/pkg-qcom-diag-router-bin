# Maintainer: Xilin Wu <sophon@radxa.com>

pkgname=qcom-diag-router-bin
pkgver=1.0.2
pkgrel=1
pkgdesc='Routing of diagnostics related messages between host and various subsystems'
arch=('aarch64')
url='https://softwarecenter.qualcomm.com'
license=('LicenseRef-Qualcomm-Proprietary')
install=diag-router.install
depends=('glib2' 'qrtr')
provides=('qcom-diag-router' 'diag')
conflicts=('qcom-diag-router' 'diag')
source=("https://softwarecenter.qualcomm.com/nexus/generic/software/chip/component/core-technologies.qclinux.0.0/260222/prebuilt_yocto/diag-router_15.0+really${pkgver}_armv8a.tar.gz"
        "diag-router.service")
sha256sums=('ec3f1c0986153ca9210a2e9b74b2b5fad3b6ae2e40678ed9e0fa2b89bdd579e6'
            'SKIP')
options=('!strip' '!debug')

package() {
    install -Dm755 usr/bin/diag-router "${pkgdir}/usr/bin/diag-router"

    install -Dm644 "${srcdir}/diag-router.service" "${pkgdir}/usr/lib/systemd/system/diag-router.service"

    install -Dm644 usr/share/doc/diag-router/LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
