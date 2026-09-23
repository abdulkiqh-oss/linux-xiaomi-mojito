
# Reference: <https://postmarketos.org/vendorkernel>
# Kernel config based on: arch/arm64/configs/(CHANGEME!)
export CARCH=aarch64 
#export SUDO_APK='abuild-apk --no-progress' 
export CROSS_COMPILE=aarch64-alpine-linux-musl- 
export CC=aarch64-alpine-linux-musl-gcc 
export RUSTC_WRAPPER=/usr/bin/sccache 
export GOCACHE=/home/pmos/.cache/go-build 
export HOME=/home/pmos


pkgname=linux-xiaomi-mojito
pkgver=4.14.190
pkgrel=0
pkgdesc="Xiaomi Redmi Note 10 kernel fork"
arch="aarch64"
_carch="arm64"
_flavor="xiaomi-mojito"
url="https://kernel.org"
license="GPL-2.0-only"
options="!strip !check !tracedeps pmb:cross-native"
makedepends="
	bash
	bc
	bison
	devicepkg-dev
	findutils
	flex
	openssl-dev
	linux-headers
	nano
	
	perl
"

# Source
_repository="linux-xiaomi-mojito"
_commit="android_kernel_xiaomi_mojito"
_config="config-$_flavor.$arch"
source="
	$pkgname-$_commit.tar::http://127.0.0.1/$_commit.tar
	$_config


"
#src/linux-xiaomi-mojito/765eaec61cf526fabdfe52cdea1ef6aa9415b993/

builddir="$srcdir/$_commit"
_outdir="../$srcdir/out"
#export defconfig = $builddir/arch/arm64/configs/mojito_defconfig
prepare() {
	default_prepare
	. downstreamkernel_prepare
}

build() {
	unset LDFLAGS
	make clean
	#mkdir -p /home/pmos/build/src/linux-xiaomi-mojito/android_kernel_xiaomi_sm6150/include/linux/
	#rm -rf  /home/pmos/build/src/android_kernel_xiaomi_sm6150/include/linux/compiler-gcc.h
	#cp /home/pmos/build/compiler-gcc.h /home/pmos/build/src/android_kernel_xiaomi_sm6150/include/linux/compiler-gcc.h
	make  O="$_outdir" CONFIG_LITTLE_CPU_MASK=63 ARCH="$_carch" CC="${CC:-gcc}" \
		KBUILD_BUILD_VERSION="$((pkgrel + 1 ))-postmarketOS"
}

package() {
	downstreamkernel_package "$builddir" "$pkgdir" "$_carch" \
		"$_flavor" "$_outdir"
}

sha512sums="
33f5f337a774d6daf2fb3dba82997caa4f9adc9b308024f808de5108b34dbf2d0142a0d6e8030f90fdf9ecfc845ef1b634e0fc8a92040a4ffe55759cca5f5b52  linux-xiaomi-mojito-android_kernel_xiaomi_mojito.tar
0e3632dda25445b527df03db158756d6eac4c13d2a1a8bd2d57dc2b9ca5cad71dee1d5cf1c65f7f090e7ec24c0e8a567cbcad3ef3a1f31f12d961a26eb0a1e36  config-xiaomi-mojito.aarch64

"
#bfc4187665344e4640c2f37c35ddb7180915abe96f9626a79b14fe12964003a7331008a0649a30b97588bcbc87b02ec90168394b9614e1fadf855de1e4c2fc0e  linux-xiaomi-mojito-android_kernel_xiaomi_sm6150.tar
# 93584bb9929f7a04ac8f7468af9deb63de5bcb440a2f8602e9ebe6d1346c3c7f89378b3094b99217e29d54f2987cff4d79be50f45d9b74c75141fc6cf1f55d96  linux-xiaomi-mojito-android_kernel_xiaomi_sunny.tar
#2b48f1bf0e3f70703d2cdafc47d5e615cc7c56c70bec56b2e3297d3fa4a7a1321d649a8679614553dde8fe52ff1051dae38d5990e3744c9ca986d92187dcdbeb  gcc10-extern_YYLOC_global_declaration.patch
#77eba606a71eafb36c32e9c5fe5e77f5e4746caac292440d9fb720763d766074a964db1c12bc76fe583c5d1a5c864219c59941f5e53adad182dbc70bf2bc14a7  gcc7-give-up-on-ilog2-const-optimizations.patch
#197d40a214ada87fcb2dfc0ae4911704b9a93354b75179cd6b4aadbb627a37ec262cf516921c84a8b1806809b70a7b440cdc8310a4a55fca5d2c0baa988e3967  gcc8-fix-put-user.patch
#ad0182a483791fc88e058838bc331b2f04a75ba291e763767babdb815efadfc3b4fda97e69e2e3f00a426cabea088e35297a92bd287592597d1e309be68ee92c  kernel-use-the-gnu89-standard-explicitly.patch

#gcc7-give-up-on-ilog2-const-optimizations.patch
        #gcc8-fix-put-user.patch
        #gcc10-extern_YYLOC_global_declaration.patch
        #kernel-use-the-gnu89-standard-explicitly.patch




#/home/pmos/build/src/linux-xiaomi-mojito/765eaec61cf526fabdfe52cdea1ef6aa9415b993/include/linux/compiler.h
#/home/pmos/build/src/linux-xiaomi-mojito/765eaec61cf526fabdfe52cdea1ef6aa9415b993/tools/virtio/linux/compiler.h
#/home/pmos/build/src/linux-xiaomi-mojito/765eaec61cf526fabdfe52cdea1ef6aa9415b993/tools/include/linux/compiler.h





















































# # Reference: <https://postmarketos.org/vendorkernel>
# # Kernel config based on: arch/arm64/configs/(CHANGEME!)

# pkgname=linux-xiaomi-mojito
# pkgver=4.14.190
# pkgrel=0
# pkgdesc="Xiaomi Redmi Note 10 kernel fork"
# arch="aarch64"
# _carch="arm64"
# _flavor="xiaomi-mojito"
# url="https://kernel.org"
# license="GPL-2.0-only"
# options="!strip !check !tracedeps pmb:cross-native"
# makedepends="
# 	bash
# 	bc
# 	bison
# 	devicepkg-dev
# 	findutils
# 	flex
# 	openssl-dev
# 	perl
# "

# # Source
# _repository="linux-xiaomi-mojito"
# _commit="765eaec61cf526fabdfe52cdea1ef6aa9415b993"
# _config="config-$_flavor.$arch"
# source="
# 	$pkgname-$_commit.tar.gz::http://127.0.0.1/$_commit.tar.gz
# 	$_config
# 	gcc7-give-up-on-ilog2-const-optimizations.patch
# 	gcc8-fix-put-user.patch
# 	gcc10-extern_YYLOC_global_declaration.patch
# 	kernel-use-the-gnu89-standard-explicitly.patch
# "
# builddir="$srcdir/$_repository-$_commit"
# _outdir="out"

# prepare() {
# 	default_prepare
# 	. downstreamkernel_prepare
# }

# build() {
# 	unset LDFLAGS
# 	make O="$_outdir" ARCH="$_carch" CC="${CC:-gcc}" \
# 		KBUILD_BUILD_VERSION="$((pkgrel + 1 ))-postmarketOS"
# }

# package() {
# 	downstreamkernel_package "$builddir" "$pkgdir" "$_carch" \
# 		"$_flavor" "$_outdir"
# }

# sha512sums="a10a0a92bc9d4081f70d62e940c5fd47b9a6358861f844d76101c1f79554d33de32ccd5b1ec5d74b6d0c70a83fa50b2336c8eba4c8d9ec271e5f01a6ce8a2b71  765eaec61cf526fabdfe52cdea1ef6aa9415b993.tar.gz
# 2596f9c102d8409c91b28db2c3ed29acd900633104bde804065f55cf60e7b6c744fc2870b5a3ced2e491062be5fe65cc82be11a48dda85846767ce3d35451ff2  config-xiaomi-mojito.aarch64
# 2b48f1bf0e3f70703d2cdafc47d5e615cc7c56c70bec56b2e3297d3fa4a7a1321d649a8679614553dde8fe52ff1051dae38d5990e3744c9ca986d92187dcdbeb  gcc10-extern_YYLOC_global_declaration.patch
# 77eba606a71eafb36c32e9c5fe5e77f5e4746caac292440d9fb720763d766074a964db1c12bc76fe583c5d1a5c864219c59941f5e53adad182dbc70bf2bc14a7  gcc7-give-up-on-ilog2-const-optimizations.patch
# 197d40a214ada87fcb2dfc0ae4911704b9a93354b75179cd6b4aadbb627a37ec262cf516921c84a8b1806809b70a7b440cdc8310a4a55fca5d2c0baa988e3967  gcc8-fix-put-user.patch
# ad0182a483791fc88e058838bc331b2f04a75ba291e763767babdb815efadfc3b4fda97e69e2e3f00a426cabea088e35297a92bd287592597d1e309be68ee92c  kernel-use-the-gnu89-standard-explicitly.patch

# "
