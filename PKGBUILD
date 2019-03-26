# Maintainer: Marc Plano-Lesay <marc.planolesay@gmail.com>

pkgname="bazelisk"
pkgver="0.0.3"
pkgrel="1"
pkgdesc="A user-friendly launcher for Bazel."
arch=("i686" "x86_64")
license=("Apache 2.0")
url="https://github.com/philwo/bazelisk"
makedepends=("bazel")

source=("bazelisk.tar.gz::$url/archive/v$pkgver.tar.gz")
sha256sums=("2a48d971eb8bca06bf95f6b8fd4309f827749869a702a1f00709ac2f28b143dd")

build() {
  cd bazelisk-$pkgver
  bazel build //:bazelisk
}

package() {
  cd bazelisk-$pkgver
  install -Dm755 bazel-bin/*/bazelisk "$pkgdir"/usr/bin/bazelisk
  install -Dm644 LICENSE "$pkgdir"/usr/share/licenses/bazelisk/LICENSE
}

