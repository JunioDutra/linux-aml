# Khadas Patched AArch64 multi-platform Kernel
# Maintainer: Furkan Kardame <furkan@fkardame.com>

pkgbase=linux-khadas
_srcname=linux-5.19
_kernelname=${pkgbase#linux}
_desc="AArch64 multi-platform"
pkgver=5.19.17
pkgrel=1
arch=('aarch64')
url="http://www.kernel.org/"
license=('GPL2')
makedepends=('xmlto' 'docbook-xsl' 'kmod' 'inetutils' 'bc' 'git' 'dtc')
options=('!strip')
source=("http://www.kernel.org/pub/linux/kernel/v5.x/${_srcname}.tar.xz"
        "http://www.kernel.org/pub/linux/kernel/v5.x/patch-${pkgver}.xz"
        'config'
        'linux.preset'
        '60-linux.hook'
        '90-linux.hook'
	'0001-HACK-set-meson-gx-cma-pool-to-896MB.patch'
	'0002-HACK-set-meson-g12-cma-pool-to-896MB.patch'
	'0003-HACK-arm64-fix-Kodi-sysinfo-CPU-information.patch'
	'0004-HACK-arm64-dts-meson-gx-add-ATF-BL32-reserved-memory.patch'
	'0005-HACK-arm64-meson-add-Amlogic-Meson-GX-PM-Suspend.patch'
	'0006-HACK-arm64-dts-meson-add-support-for-GX-PM-and-Virtu.patch'
	'0007-HACK-arm64-dts-meson-add-rtc-vrtc-aliases-to-Khadas-.patch'
	'0008-HACK-of-partial-revert-of-fdt.c-changes.patch'
	'0014-WIP-mmc-meson-gx-mmc-set-core-clock-phase-to-270-deg.patch'
	'0015-WIP-media-meson-vdec-remove-redundant-if-statement.patch'
	'0016-WIP-drivers-meson-vdec-improve-mmu-and-fbc-handling-.patch'
	'0017-WIP-drivers-meson-vdec-add-hevc-decode-codec.patch'
	'0018-WIP-drivers-meson-vdec-add-handling-to-HEVC-decoder-.patch'
	'0019-WIP-ASoC-hdmi-codec-reorder-channel-allocation-list.patch'
	'0020-WIP-ASoC-meson-aiu-encoder-spdif-implement-the-.mute.patch'
	'0021-WIP-ASoC-meson-aiu-encoder-i2s-implement-the-.mute_s.patch'
	'0022-WIP-ALSA-pcm-fix-ELD-constraints-for-some-compressed.patch'
	'0023-WIP-ALSA-pcm-ignore-formats-not-supported-by-kodi-in.patch'
	'0024-media-rc-add-common-keymap-for-Dreambox-RC10-and-RC2.patch'
	'0025-arm64-dts-meson-add-common-SM1-ac2xx-dtsi.patch'
	'0026-WIP-arm64-dts-meson-add-common-hdmi-hdmi-spdif-dtsi-.patch'
	'0027-WIP-arm64-dts-meson-add-common-hdmi-hdmi-spdif-dtsi-.patch'
	'0028-WIP-arm64-dts-meson-add-audio-playback-to-khadas-vim.patch'
	'0029-rockchip_khadas_edge_add_missed_spiflash.patch'
	'0030-rockchip_khadas_edge_add_ir_recv.patch'
	'0031-arm64-dts-VIM3-VIM3L-fix-memory-size-for-vendor-u-bo.patch'
	'0032-arm64-dts-VIM2-fix-broken-ethernet-interface-up-down.patch'
	'0033-VIM3-hack-for-PCIe.patch'
	'0034-ETH-setup-mac-address-from-command-line.patch'
	'0035-VIM3-Change-fan-auto-control-temp-to-50-C.patch'
	'0037-Revert-builddeb-Fix-rootless-build-in-setuid-setgid-.patch'
	'0038-Revert-builddeb-Enable-rootless-builds.patch'
	'0039-packaging-5.x-with-postinstall-scripts.patch'
	'0040-builddeb-update-dtb-file-for-SD-images.patch'
	'0041-Add-text_offset.patch'
	'0042-VIMs-add-gpiomem-support.patch'
	'0043-add-device-model-to-proc-cpuinfo.patch'
	'0045-arm64-dts-VIM3-3L-add-serial-aliases.patch'
	'0046-arm64-dts-VIM1-update-serial-aliases.patch'
	'0047-arm64-dts-VIM2-update-serial-aliases.patch'
	'0048-arm64-dts-VIM3-3L-add-i2c-aliases.patch'
	'0049-VIM1-2-add-i2c-aliases.patch'
	'0051-arm64-dts-VIM3L-add-npu-node.patch'
	'0052-arm64-dts-VIM3-add-npu-node.patch'
	'0058-watchdog-meson_gxbb_wdt-remove-stop_on_reboot.patch'
	'0059-arm64-dts-meson-sm1-khadas-vim3l-use-one-sound-node-.patch'
	'0060-arm64-dts-meson-add-spdif-out-to-khadas-vim.patch'
	'0061-arm64-dts-meson-add-spdif-out-to-khadas-vim2.patch'
	'0062-arm64-dts-meson-sm1-add-spdifin-spdifout-nodes.patch'
	'0063-arm64-dts-meson-khadas-vim3-remake-simple-sound-for-.patch'
	'0064-arm64-dts-meson-add-initial-Beelink-GT1-Ultimate-dev.patch'
    	'0065-add-ugoos-device.patch'
    	'0066-drm-meson-add-YUV422-output-support.patch'
	'0067-drm-meson-encoder-add-YUV422-output-support.patch'
	'v1-0001-PCI-add-PCIe-Max-Read-Request-Size.patch'
	'v1-0002-PCI-DWC-meson-setup-512-PCIe-Max-Read-Request-Siz.patch'
	'v2-0001-arm64-dts-rockchip-remove-mmc-hs400-enhanced-stro.patch'
	'v4-0001-of-add-Overlay-ConfigFS-interface.patch'
	'v5-0001-dtb-enable-creation-of-__symbols__-node.patch'
	'832f662660986d9707e5768541a72fb03b85d099.patch'
	'https://github.com/spikerguy/linux/commit/a2eef8635c0a9f3d831bcddb3368117981599e70.patch'
	'https://github.com/spikerguy/linux/commit/b5b067c1c6ad34c5d15729d2147781f6f14549ad.patch'
	'0001-arm64-dts-meson-radxa-zero-add-support-for-the-usb-t.patch'
	'0002-pinctrl-meson-Add-several-missing-pinmux-for-pwm-fun.patch'
	'0003-dt-bindings-arm-amlogic-add-support-for-Radxa-Zero2.patch'
	'0004-arm64-dts-meson-add-support-for-Radxa-Zero2.patch')

md5sums=('f91bfe133d2cb1692f705947282e123a'
         '89a5211f788791b511c149374d68c48f'
         'e2745a8998b4be38f9c664668966561a'
         '86d4a35722b5410e3b29fc92dae15d4b'
         'ce6c81ad1ad1f8b333fd6077d47abdaf'
         '3dc88030a8f2f5a5f97266d99b149f77'
         '0e28a6bf6c8b4e33f47acdde66847a62'
         '9d467258b9775de03b9ddc11797ac67d'
         'cf80d02a3d91e0d23c4a4d0e4801e16c'
         'd3dda8af332f6b921fd10b7ba08fb062'
         '18635585ff38cdaf73bc7a94ba7eebaf'
         '14c1ff44d252e0a35ad0bf302035a321'
         'e35270deb534fca477b237621bdba3e6'
         '8d8471b38cd0e0a1dc4d7f9a9e0a292c'
         'c8444872bf7670e72b1028265ea71185'
         '78abeb86982c3a3aeb147d29dcc3ca83'
         'bc513edabed56f544b4b78413e490422'
         '693332564e06ec09086faf1a2e1b4f63'
         '4e1546d1aba4b982d1683fc004df836e'
         'b76c3b61ae29b2d5de6611b97d8c8a9b'
         '6df6ab67320910f6cbc734eaae5be3e0'
         'db8bc109ca76f3638819fe798dd2255e'
         'a2d2527e668f705e662210db7a639ef1'
         '6834be0b532afb3ff7bb48d47755d822'
         '4747aef0e9a97aa37ca99efe147d0b35'
         '183f9851253aa09774231cee7ce8abce'
         '4d77455d6dd9257bc30a1c42e28dba90'
         '64fe9f48e9fc47df224f219224e0eaf8'
         'd2b695541e7927fa37cb349d121d4af7'
         '5bbf0a070a47d5daf87795355fdf93be'
         '00e9ccefe6dbb4ba6e7a3c8f10f99828'
         '4e85f7840f906e3a8ff6a4e62516f64b'
         '8fff17240ad0ca0335e65a584b130142'
         'c78bf349331f51829913594d9d1fbe0a'
         'dd2680f4cbf2024f48ed1bd637fcc952'
         'f4c97210987e7076a3442f3135a5f2bc'
         'ada2ba969253b19f02377dcf78ce4f9f'
         'ecd4c255fc699c499f62f74ee3b8a32b'
         'a08826d49d32db75ec30aa8eae2c869f'
         '05ffd1df2326dc7e4ccf483879e02720'
         '04cc3a41b286779343c7fd0f06b78b13'
         '2aefe2be17c2097ec5fabc6a6e6ad2f8'
         'c0524f5ded54f98b5345e01b54d2795a'
         '2325eec6a894a02f117e15520ddb1515'
         '0a2c23dee0e70306b9384a4142b40025'
         '279e608ccebb23c56d25a4909c505e2f'
         'dba377b62ca9d129e46a11fd1bf6fe7c'
         '5794ae1f3caecd85fac4f42a6892754e'
         'e291b444d6c1d5b68494787a133fd95c'
         '52029f8f2aee55e06200c9fcfa3b1492'
         'b55c465906bbfc09b51062a27b3d885c'
         'aacbc002fc5bbaa903c72b1fd1d44292'
         'cdc74b27c6742a0c88592359045828ff'
         'df7b3db97e601766d8280a685e12ccc4'
         '2e16f477544723d4709f1f7b117e6ae9'
         'da1ae27bf11081c277a8b504f5033297'
         '0910789410d92d3ae21996a66f45f041'
         '1b92d7617e60d3c525a4b18ab4351185'
         '469417b64e6a2bf65bd74c6d9cad2040'
         '47ebd261e31fe881abafee88c9d33767'
         '00e5055ecbdd583cab132d885f11a290'
         '607269265296f7391f02d75e9076033e'
         '8ea473f5a69781f37b0415ff3a728832'
         'fcaa04a94040f734f8fd2347f1d28d3a'
         '16101539fa994e9ac2adb51ff92776ae'
         '8e5c7790d65a87606d2d34295d5a0a65'
         '5c50db3f0888d80ecc2be4351879b1f6'
         'e4d32fa4336b46524597a3bbc715d272'
         '9799998aa9b72fae2eb55e92d840dad5'
         '2a971540beded13ca4c9bc0123ca563b'
         'b5f364a62760483df0af20c7bf6ddb0d'
         'd7f846f361d538be6ab2d7a2066774e2')

prepare() {
  cd ${_srcname}

  # add upstream patch
  patch -Np1 -i "${srcdir}/patch-${pkgver}"

  # Khadas patches
  patch -Np1 -i "${srcdir}/0001-HACK-set-meson-gx-cma-pool-to-896MB.patch"
  patch -Np1 -i "${srcdir}/0002-HACK-set-meson-g12-cma-pool-to-896MB.patch"
  #patch -Np1 -i "${srcdir}/0003-HACK-arm64-fix-Kodi-sysinfo-CPU-information.patch"
  #patch -Np1 -i "${srcdir}/0004-HACK-arm64-dts-meson-gx-add-ATF-BL32-reserved-memory.patch"	#Creates Duplicate nodes
  #patch -Np1 -i "${srcdir}/0005-HACK-arm64-meson-add-Amlogic-Meson-GX-PM-Suspend.patch"
  #patch -Np1 -i "${srcdir}/0006-HACK-arm64-dts-meson-add-support-for-GX-PM-and-Virtu.patch"
  #patch -Np1 -i "${srcdir}/0007-HACK-arm64-dts-meson-add-rtc-vrtc-aliases-to-Khadas-.patch"
  #patch -Np1 -i "${srcdir}/0008-HACK-of-partial-revert-of-fdt.c-changes.patch"
  patch -Np1 -i "${srcdir}/0014-WIP-mmc-meson-gx-mmc-set-core-clock-phase-to-270-deg.patch"
  patch -Np1 -i "${srcdir}/0015-WIP-media-meson-vdec-remove-redundant-if-statement.patch"
  patch -Np1 -i "${srcdir}/0016-WIP-drivers-meson-vdec-improve-mmu-and-fbc-handling-.patch"
  patch -Np1 -i "${srcdir}/0017-WIP-drivers-meson-vdec-add-hevc-decode-codec.patch"
  patch -Np1 -i "${srcdir}/0018-WIP-drivers-meson-vdec-add-handling-to-HEVC-decoder-.patch"
  #patch -Np1 -i "${srcdir}/0019-WIP-ASoC-hdmi-codec-reorder-channel-allocation-list.patch"
  #patch -Np1 -i "${srcdir}/0020-WIP-ASoC-meson-aiu-encoder-spdif-implement-the-.mute.patch"
  #patch -Np1 -i "${srcdir}/0021-WIP-ASoC-meson-aiu-encoder-i2s-implement-the-.mute_s.patch"
  #patch -Np1 -i "${srcdir}/0022-WIP-ALSA-pcm-fix-ELD-constraints-for-some-compressed.patch"
  #patch -Np1 -i "${srcdir}/0023-WIP-ALSA-pcm-ignore-formats-not-supported-by-kodi-in.patch"
  patch -Np1 -i "${srcdir}/0024-media-rc-add-common-keymap-for-Dreambox-RC10-and-RC2.patch"
  #patch -Np1 -i "${srcdir}/0025-arm64-dts-meson-add-common-SM1-ac2xx-dtsi.patch"			# Applied in 5.18.1
  #patch -Np1 -i "${srcdir}/0026-WIP-arm64-dts-meson-add-common-hdmi-hdmi-spdif-dtsi-.patch"
  #patch -Np1 -i "${srcdir}/0027-WIP-arm64-dts-meson-add-common-hdmi-hdmi-spdif-dtsi-.patch"
  #patch -Np1 -i "${srcdir}/0028-WIP-arm64-dts-meson-add-audio-playback-to-khadas-vim.patch"
  patch -Np1 -i "${srcdir}/0029-rockchip_khadas_edge_add_missed_spiflash.patch"
  patch -Np1 -i "${srcdir}/0030-rockchip_khadas_edge_add_ir_recv.patch"
  patch -Np1 -i "${srcdir}/0031-arm64-dts-VIM3-VIM3L-fix-memory-size-for-vendor-u-bo.patch"
  patch -Np1 -i "${srcdir}/0032-arm64-dts-VIM2-fix-broken-ethernet-interface-up-down.patch"
  patch -Np1 -i "${srcdir}/0033-VIM3-hack-for-PCIe.patch"
  patch -Np1 -i "${srcdir}/0034-ETH-setup-mac-address-from-command-line.patch"
  patch -Np1 -i "${srcdir}/0035-VIM3-Change-fan-auto-control-temp-to-50-C.patch"
  #patch -Np1 -i "${srcdir}/0037-Revert-builddeb-Fix-rootless-build-in-setuid-setgid-.patch"
  #patch -Np1 -i "${srcdir}/0038-Revert-builddeb-Enable-rootless-builds.patch"
  #patch -Np1 -i "${srcdir}/0039-packaging-5.x-with-postinstall-scripts.patch"
  #patch -Np1 -i "${srcdir}/0040-builddeb-update-dtb-file-for-SD-images.patch"
  #patch -Np1 -i "${srcdir}/0041-Add-text_offset.patch"
  patch -Np1 -i "${srcdir}/0042-VIMs-add-gpiomem-support.patch"
  #patch -Np1 -i "${srcdir}/0043-add-device-model-to-proc-cpuinfo.patch"
  patch -Np1 -i "${srcdir}/0045-arm64-dts-VIM3-3L-add-serial-aliases.patch"
  patch -Np1 -i "${srcdir}/0046-arm64-dts-VIM1-update-serial-aliases.patch"
  patch -Np1 -i "${srcdir}/0047-arm64-dts-VIM2-update-serial-aliases.patch"
  patch -Np1 -i "${srcdir}/0048-arm64-dts-VIM3-3L-add-i2c-aliases.patch"
  patch -Np1 -i "${srcdir}/0049-VIM1-2-add-i2c-aliases.patch"
  patch -Np1 -i "${srcdir}/0051-arm64-dts-VIM3L-add-npu-node.patch"
  patch -Np1 -i "${srcdir}/0052-arm64-dts-VIM3-add-npu-node.patch"
  #patch -Np1 -i "${srcdir}/0058-watchdog-meson_gxbb_wdt-remove-stop_on_reboot.patch"
  #patch -Np1 -i "${srcdir}/0059-arm64-dts-meson-sm1-khadas-vim3l-use-one-sound-node-.patch"
  patch -Np1 -i "${srcdir}/0060-arm64-dts-meson-add-spdif-out-to-khadas-vim.patch"
  patch -Np1 -i "${srcdir}/0061-arm64-dts-meson-add-spdif-out-to-khadas-vim2.patch"
  #patch -Np1 -i "${srcdir}/0062-arm64-dts-meson-sm1-add-spdifin-spdifout-nodes.patch"
  #patch -Np1 -i "${srcdir}/0063-arm64-dts-meson-khadas-vim3-remake-simple-sound-for-.patch"
  patch -Np1 -i "${srcdir}/0064-arm64-dts-meson-add-initial-Beelink-GT1-Ultimate-dev.patch"
  patch -Np1 -i "${srcdir}/0065-add-ugoos-device.patch"
  patch -Np1 -i "${srcdir}/0067-drm-meson-encoder-add-YUV422-output-support.patch"
  patch -Np1 -i "${srcdir}/v1-0001-PCI-add-PCIe-Max-Read-Request-Size.patch"
  patch -Np1 -i "${srcdir}/v1-0002-PCI-DWC-meson-setup-512-PCIe-Max-Read-Request-Siz.patch"
  #patch -Np1 -i "${srcdir}/v2-0001-arm64-dts-rockchip-remove-mmc-hs400-enhanced-stro.patch" 	#Already applied on 5.15.11
  #patch -Np1 -i "${srcdir}/v4-0001-of-add-Overlay-ConfigFS-interface.patch"
  patch -Np1 -i "${srcdir}/a2eef8635c0a9f3d831bcddb3368117981599e70.patch"			#Add GPIO Fan control GS King X
  patch -Np1 -i "${srcdir}/b5b067c1c6ad34c5d15729d2147781f6f14549ad.patch" 			#GPIO Fan to only use single cooling map
  patch -Np1 -i "${srcdir}/0001-arm64-dts-meson-radxa-zero-add-support-for-the-usb-t.patch"	# USB-C Support for Zero
  patch -Np1 -i "${srcdir}/0002-pinctrl-meson-Add-several-missing-pinmux-for-pwm-fun.patch"	# Pinmux for Zero2
  patch -Np1 -i "${srcdir}/0003-dt-bindings-arm-amlogic-add-support-for-Radxa-Zero2.patch"
  patch -Np1 -i "${srcdir}/0004-arm64-dts-meson-add-support-for-Radxa-Zero2.patch"		# Add Zero2 support
  
  cat "${srcdir}/config" > ./.config

  # add pkgrel to extraversion
  sed -ri "s|^(EXTRAVERSION =)(.*)|\1 \2-${pkgrel}|" Makefile

  # don't run depmod on 'make install'. We'll do this ourselves in packaging
  sed -i '2iexit 0' scripts/depmod.sh
  #make menuconfig
  #cp ./.config "${srcdir}/config"

}

build() {
  cd ${_srcname}

  # get kernel version
  make prepare

  # load configuration
  # Configure the kernel. Replace the line below with one of your choice.
  #make menuconfig # CLI menu for configuration
  #make nconfig # new CLI menu for configuration
  #make xconfig # X-based configuration
  #make oldconfig # using old config from previous kernel version
  # ... or manually edit .config

  # Copy back our configuration (use with new kernel version)
  #cp ./.config /var/tmp/${pkgbase}.config

  ####################
  # stop here
  # this is useful to configure the kernel
  #msg "Stopping build"
  #return 1
  ####################

  #yes "" | make config

  # build!
  unset LDFLAGS
  make ${MAKEFLAGS} Image modules Image.gz
  # Generate device tree blobs with symbols to support applying device tree overlays in U-Boot
  make ${MAKEFLAGS} DTC_FLAGS="-@" dtbs
}

_package() {
  pkgdesc="The Linux Kernel and modules - ${_desc}"
  depends=('coreutils' 'linux-firmware' 'kmod' 'mkinitcpio>=0.7')
  optdepends=('crda: to set the correct wireless channels of your country')
  provides=('kernel26' "linux=${pkgver}")
  conflicts=('kernel26' 'linux')
  replaces=('linux-armv8' 'linux-aarch64')
  backup=("etc/mkinitcpio.d/${pkgbase}.preset")
  install=${pkgname}.install

  cd ${_srcname}

  KARCH=arm64

  # get kernel version
  _kernver="$(make kernelrelease)"
  _basekernel=${_kernver%%-*}
  _basekernel=${_basekernel%.*}

  mkdir -p "${pkgdir}"/{boot,usr/lib/modules}
  make INSTALL_MOD_PATH="${pkgdir}/usr" modules_install
  make INSTALL_DTBS_PATH="${pkgdir}/boot/dtbs" dtbs_install
  cp arch/$KARCH/boot/Image "${pkgdir}/boot"

  # make room for external modules
  local _extramodules="extramodules-${_basekernel}${_kernelname}"
  ln -s "../${_extramodules}" "${pkgdir}/usr/lib/modules/${_kernver}/extramodules"

  # add real version for building modules and running depmod from hook
  echo "${_kernver}" |
    install -Dm644 /dev/stdin "${pkgdir}/usr/lib/modules/${_extramodules}/version"

  # remove build and source links
  rm "${pkgdir}"/usr/lib/modules/${_kernver}/{source,build}

  # now we call depmod...
  depmod -b "${pkgdir}/usr" -F System.map "${_kernver}"


  # sed expression for following substitutions
  local _subst="
    s|%PKGBASE%|${pkgbase}|g
    s|%KERNVER%|${_kernver}|g
    s|%EXTRAMODULES%|${_extramodules}|g
  "

  # install mkinitcpio preset file
  sed "${_subst}" ../linux.preset |
    install -Dm644 /dev/stdin "${pkgdir}/etc/mkinitcpio.d/${pkgbase}.preset"

  # install pacman hooks
  sed "${_subst}" ../60-linux.hook |
    install -Dm644 /dev/stdin "${pkgdir}/usr/share/libalpm/hooks/60-${pkgbase}.hook"
  sed "${_subst}" ../90-linux.hook |
    install -Dm644 /dev/stdin "${pkgdir}/usr/share/libalpm/hooks/90-${pkgbase}.hook"
}

_package-headers() {
  pkgdesc="Header files and scripts for building modules for linux kernel - ${_desc}"
  provides=("linux-headers=${pkgver}")
  conflicts=('linux-headers')
  replaces=('linux-aarch64-headers')

  cd ${_srcname}
  local _builddir="${pkgdir}/usr/lib/modules/${_kernver}/build"

  install -Dt "${_builddir}" -m644 Makefile .config Module.symvers
  install -Dt "${_builddir}/kernel" -m644 kernel/Makefile

  mkdir "${_builddir}/.tmp_versions"

  cp -t "${_builddir}" -a include scripts

  install -Dt "${_builddir}/arch/${KARCH}" -m644 arch/${KARCH}/Makefile
  install -Dt "${_builddir}/arch/${KARCH}/kernel" -m644 arch/${KARCH}/kernel/asm-offsets.s
  install -Dt "${_builddir}" -m644 vmlinux 

  cp -t "${_builddir}/arch/${KARCH}" -a arch/${KARCH}/include
  mkdir -p "${_builddir}/arch/arm"
  cp -t "${_builddir}/arch/arm" -a arch/arm/include

  install -Dt "${_builddir}/drivers/md" -m644 drivers/md/*.h
  install -Dt "${_builddir}/net/mac80211" -m644 net/mac80211/*.h

  # http://bugs.archlinux.org/task/13146
  install -Dt "${_builddir}/drivers/media/i2c" -m644 drivers/media/i2c/msp3400-driver.h

  # http://bugs.archlinux.org/task/20402
  install -Dt "${_builddir}/drivers/media/usb/dvb-usb" -m644 drivers/media/usb/dvb-usb/*.h
  install -Dt "${_builddir}/drivers/media/dvb-frontends" -m644 drivers/media/dvb-frontends/*.h
  install -Dt "${_builddir}/drivers/media/tuners" -m644 drivers/media/tuners/*.h

  # add xfs and shmem for aufs building
  mkdir -p "${_builddir}"/{fs/xfs,mm}

  # copy in Kconfig files
  find . -name Kconfig\* -exec install -Dm644 {} "${_builddir}/{}" \;

  # remove unneeded architectures
  local _arch
  for _arch in "${_builddir}"/arch/*/; do
    [[ ${_arch} == */${KARCH}/ || ${_arch} == */arm/ ]] && continue
    rm -r "${_arch}"
  done

  # remove documentation files
  rm -r "${_builddir}/Documentation"

  # remove now broken symlinks
  find -L "${_builddir}" -type l -printf 'Removing %P\n' -delete

  # strip scripts directory
  local file
  while read -rd '' file; do
    case "$(file -bi "$file")" in
      application/x-sharedlib\;*)      # Libraries (.so)
        strip $STRIP_SHARED "$file" ;;
      application/x-archive\;*)        # Libraries (.a)
        strip $STRIP_STATIC "$file" ;;
      application/x-executable\;*)     # Binaries
        strip $STRIP_BINARIES "$file" ;;
      application/x-pie-executable\;*) # Relocatable binaries
        strip $STRIP_SHARED "$file" ;;
    esac
  done < <(find "${_builddir}" -type f -perm -u+x ! -name vmlinux -print0 2>/dev/null)
  strip $STRIP_STATIC "${_builddir}/vmlinux"
  
  # remove unwanted files
  find ${_builddir} -name '*.orig' -delete
}

pkgname=("${pkgbase}" "${pkgbase}-headers")
for _p in ${pkgname[@]}; do
  eval "package_${_p}() {
    _package${_p#${pkgbase}}
  }"
done
