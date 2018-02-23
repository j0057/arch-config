# Maintainer: Joost Molenaar <jjm@j0057.nl>
pkgbase=j0057-cfg
pkgname=(
    j0057-cfg-base
    j0057-cfg-ntp
    j0057-cfg-pi-rngd
)
pkgver=0.1
pkgrel=1
epoch=
pkgdesc="Metapackages for j0057 his Arch systems"
arch=(any)
url="https://github.com/arch-configs"
license=(GPL)

source=(
    editor.sh
    ntpd.hook
    ntp-client.conf
    pi-rngd.conf
    sudo-wheel.conf
    vimrc
)

package_j0057-cfg-base() {
    depends=(
        bind-utils
        curl
        htop
        lsof
        strace
        sudo
        tcpdump
        vim
    )
    install=$pkgname.install

    install -D -m 644 editor.sh             $pkgdir/etc/profile.d/editor.sh
    install -D -m 644 sudo-wheel.conf       $pkgdir/etc/sudoers.d/wheel
    install -D -m 644 vimrc                 $pkgdir/etc/vimrc.j0057
}

package_j0057-cfg-ntp() {
    depends=(ntp)
    install=$pkgname.install

    install -D -m 644 ntpd.hook             $pkgdir/etc/pacman.d/hooks/ntpd.hook
    install -D -m 644 ntp-client.conf       $pkgdir/etc/ntp.conf.j0057
}

package_j0057-cfg-pi-rngd() {
    depends=(rng-tools)
    install=$pkgname.install

    install -D -m 644 pi-rngd.conf          $pkgdir/etc/conf.d/rngd.j0057
}

sha256sums=('bd0f56b7a693b0d2ff0a98c8fc0bdc1e3cd558ba57afb607615bfb2a637d22b0'
            'b2c5e0434f3b76f0614cebc4b8f01313cb57438820291afd586c590d71cf61b9'
            '0908b9b77ed3a4edae05f65a5e38197632d773fa9d788f09de08ee960470f77c'
            '9751273f49c9c258be333e689f222a0aa0e0571f416ebe09799cdb5eb3780cd2'
            '6b4c40d177f490829fb5f2507d8bb8bcd8767b92f20230e0f95637d601be809d'
            '8895d4b6ca98fd5bdc08620c3b677a5a887506187af88f559c254e194529f25a')
