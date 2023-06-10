# Khadas Patched AArch64 multi-platform Kernel
# Maintainer: Furkan Kardame <furkan@fkardame.com>

pkgbase=linux-aml
_kernelname=${pkgbase#linux}
_desc="AArch64 multi-platform"
pkgver=6.1.33
pkgrel=1
_srcname="linux-${pkgver/%.0/}"
arch=('aarch64')
url="http://www.kernel.org/"
license=('GPL2')
makedepends=('xmlto' 'docbook-xsl' 'kmod' 'inetutils' 'bc' 'git' 'dtc')
options=('!strip')
conflicts=('linux' 'linux-odroid')
replaces=('linux-khadas')
source=("https://cdn.kernel.org/pub/linux/kernel/v6.x/${_srcname}.tar.xz"
	#"http://www.kernel.org/pub/linux/kernel/v6.x/${_srcname}.tar.xz"
        'config'
        'linux.preset'
        '60-linux.hook'
        '90-linux.hook'
	'1001-LE-AML-0001-LOCAL-set-meson-gx-cma-pool-to-896MB.patch'
	'1002-LE-AML-0002-LOCAL-set-meson-g12-cma-pool-to-896MB.patch'
	'1003-LE-AML-0003-LOCAL-arm64-fix-Kodi-sysinfo-CPU-information.patch'
	'1004-LE-AML-0004-LOCAL-arm64-meson-add-Amlogic-Meson-GX-PM-Suspend.patch'
	'1005-LE-AML-0005-LOCAL-arm64-dts-meson-add-support-for-GX-PM-and-Virt.patch'
	'1006-LE-AML-0006-LOCAL-arm64-dts-meson-add-rtc-vrtc-aliases-to-Khadas.patch'
	'1007-LE-AML-0007-LOCAL-arm64-dts-meson-add-rtc-vrtc-aliases-to-Khadas.patch'
	'1008-LE-AML-0008-LOCAL-arm64-dts-meson-add-rtc-vrtc-aliases-to-Minix-.patch'
	'1009-LE-AML-0009-LOCAL-ALSA-Assign-internal-PCM-chmap-ELD-IEC958-kctl.patch'
	'1010-LE-AML-0010-LOCAL-usb-hub-disable-autosuspend-for-Genesys-Logic-.patch'
	'1011-LE-AML-0011-LOCAL-of-partial-revert-of-fdt.c-changes.patch'
	#'1013-LE-AML-0013-FROMGIT-6.1-dt-bindings-arm-amlogic-add-Beelink-GT1-.patch'
	#'1014-LE-AML-0014-FROMGIT-6.1-arm64-dts-meson-add-support-for-Beelink-.patch'
	#'1014-Revert-mmc-meson-gx-add-SDIO-interrupt-support.patch'
	'1015-LE-AML-0015-FROMLIST-v2-arm64-dts-meson-make-dts-use-gpio-fan-ma.patch'
	'1016-LE-AML-0016-FROMLIST-v1-mmc-meson-gx-fix-deferred-probing.patch'
	'1017-LE-AML-0017-FROMLIST-v5-dt-bindings-vendor-prefixes-Add-Titan-Mi.patch'
	'1018-LE-AML-0018-FROMLIST-v5-dt-bindings-auxdisplay-Add-Titan-Micro-E.patch'
	'1019-LE-AML-0019-FROMLIST-v5-docs-ABI-document-tm1628-attribute-displ.patch'
	'1020-LE-AML-0020-FROMLIST-v5-auxdisplay-add-support-for-Titanmec-TM16.patch'
	'1021-LE-AML-0021-FROMLIST-v5-arm64-dts-meson-gxl-s905w-tx3-mini-add-s.patch'
	'1022-LE-AML-0022-FROMLIST-v5-MAINTAINERS-Add-entry-for-tm1628-auxdisp.patch'
	#'1023-LE-AML-0023-FROMLIST-v1-drm-bridge-dw_hdmi-fix-preference-of-RGB.patch'
	'1024-LE-AML-0024-WIP-ASoC-hdmi-codec-reorder-channel-allocation-list.patch'
	#'1025-LE-AML-0025-WIP-mmc-meson-gx-mmc-set-core-clock-phase-to-270-deg.patch'
	'1026-LE-AML-0026-WIP-arm64-dts-meson-add-Broadcom-WiFi-to-P212-dtsi.patch'
	'1027-LE-AML-0027-WIP-arm64-dts-meson-move-pwm_ef-node-in-P212-dtsi.patch'
	'1028-LE-AML-0028-WIP-arm64-dts-meson-remove-WiFi-BT-nodes-from-Khadas.patch'
	'1029-LE-AML-0029-WIP-arm64-dts-meson-set-p212-p23x-q20x-SDIO-to-100MH.patch'
	'1030-LE-AML-0030-WIP-arm64-dts-meson-add-UHS-SDIO-capabilities-to-p21.patch'
	'1031-LE-AML-0031-WIP-arm64-dts-meson-remove-SDIO-node-from-Khadas-VIM.patch'
	'1032-LE-AML-0032-WIP-arm64-dts-meson-add-audio-playback-to-S905X-P212.patch'
	'1033-LE-AML-0033-WIP-drivers-meson-vdec-remove-redundant-if-statement.patch'
	'1034-LE-AML-0034-WIP-drivers-meson-vdec-improve-mmu-and-fbc-handling-.patch'
	'1035-LE-AML-0035-WIP-drivers-meson-vdec-add-HEVC-decode-codec.patch'
	'1036-LE-AML-0036-WIP-drivers-meson-vdec-add-handling-to-HEVC-decoder-.patch'
	'1037-LE-AML-0037-WIP-drivers-meson-vdec-add-HEVC-support-to-GXBB.patch'
	'1038-LE-AML-0038-WIP-drivers-meson-vdec-check-if-parser-has-really-pa.patch'
	'1039-LE-AML-0039-WIP-arm64-dts-meson-radxa-zero-add-support-for-the-u.patch'
	'1040-LE-AML-0040-WIP-dt-bindings-arm-amlogic-add-support-for-Radxa-Ze.patch'
	'1041-LE-AML-0041-WIP-arm64-dts-meson-add-support-for-Radxa-Zero2.patch'
	'1042-LE-AML-0042-WIP-arm64-dts-meson-add-audio-playback-to-p201.patch'
	'1043-LE-AML-0043-WIP-arm64-dts-meson-add-audio-playback-to-p200.patch'
	'1044-LE-AML-0044-WIP-arm64-dts-meson-add-audio-playback-to-u200.patch'
	'1045-LE-AML-0045-WIP-arm64-dts-meson-add-Headphone-output-to-Beelink-.patch'
	'1046-LE-AML-0046-WIP-dt-bindings-arm-amlogic-add-support-for-the-Tani.patch'
	'1047-LE-AML-0047-WIP-arm64-dts-meson-add-support-for-the-Tanix-TX5-Ma.patch'
	'1048-LE-AML-0048-WIP-arm64-dts-meson-add-multiple-MeCool-device-trees.patch'
	'1049-LE-AML-0049-WIP-dt-bindings-arm-amlogic-add-support-for-Minix-NE.patch'
	'1050-LE-AML-0050-WIP-arm64-dts-meson-add-initial-device-tree-for-Mini.patch'
	'1051-LE-AML-0051-LOCAL-arm64-dts-meson-add-rtc-vrtc-aliases-to-Minix-.patch'
	'1052-LE-AML-0052-WIP-media-rc-add-keymap-for-Beelink-Mini-MXIII-remot.patch'
	'1053-LE-AML-0053-WIP-dt-bindings-arm-amlogic-add-support-for-Beelink-.patch'
	'1054-LE-AML-0054-WIP-arm64-dts-meson-add-support-for-Beelink-Mini-MXI.patch'
	'1055-LE-AML-0055-WIP-media-rc-add-keymap-for-MeCool-M8S-Pro-W-remote.patch'
	'1056-LE-AML-0056-WIP-dt-bindings-arm-amlogic-add-support-for-MeCool-M.patch'
	'1057-LE-AML-0057-WIP-arm64-dts-meson-add-support-for-MeCool-M8S-Pro-W.patch'
	'1058-LE-AML-0058-WIP-dt-bindings-arm-amlogic-add-Vero-4K-binding.patch'
	'1059-LE-AML-0059-WIP-arm64-dts-meson-add-support-for-OSMC-Vero-4K.patch'
	'1060-LE-AML-0060-WIP-arm64-dts-meson-add-RTL8822CS-bluetooth-to-X96-A.patch'
	'1061-LE-AML-0061-WIP-media-rc-add-keymap-for-Venz-V10-remote.patch'
	'1062-LE-AML-0062-WIP-dt-bindings-arm-amlogic-add-S905L-and-Venz-V10-b.patch'
	'1063-LE-AML-0063-WIP-arm64-dts-meson-add-support-for-Venz-V10.patch'
	'1064-LE-AML-0064-WIP-dt-bindings-vendor-prefixes-add-tbee-prefix.patch'
	'1065-LE-AML-0065-WIP-dt-bindings-arm-amlogic-add-TBee-Box-binding.patch'
	'1066-LE-AML-0066-WIP-arm64-dts-meson-add-support-for-TBee-Box.patch'
	'1067-LE-AML-0067-WIP-dt-bindings-arm-amlogic-add-Beelink-GT1-binding.patch'
	'1068-LE-AML-0068-WIP-arm64-dts-meson-add-support-for-Beelink-GT1.patch'
	'1069-LE-AML-0069-WIP-arm64-dts-meson-add-vcc_5v-regulator-to-WeTek-dt.patch'
	'1070-LE-AML-0070-WIP-arm64-dts-meson-add-audio-lineout-to-WeTek-Play2.patch'
	'1071-LE-AML-0071-WIP-arm64-dts-amlogic-fix-cvbs-disable-on-WeTek-Hub.patch'
	'1072-LE-AML-0072-WIP-ASoC-dt-bindings-add-compatible-for-es8323-i2c.patch'
	'1073-LE-AML-0073-WIP-ASoC-codecs-add-support-for-ES8323.patch'
	'2001-VIM3-hack-for-PCIe.patch'
	'2002-VIM3-Change-fan-auto-control-temp-to-50-C.patch'                               	# Vim3 Fan control
	'2004-add-ugoos-upstream.patch'
	#'2004-add-ugoos-device.patch'								# Ugoos AM6
	"2005-arm64-dts-gxkingx-gpio-fan1.patch::https://github.com/spikerguy/linux/commit/a2eef8635c0a9f3d831bcddb3368117981599e70.patch"	# GSKing X GPIO Fan
	"2006-arm64-dts-gxkingx-gpio-fan2.patch::https://github.com/spikerguy/linux/commit/b5b067c1c6ad34c5d15729d2147781f6f14549ad.patch"	# GSKing X GPIO Fan
	"2007-arm64-dts-amlogic-add-g1-tiny-pc-s905x3-support.patch")
md5sums=('c9289d53bc6217ad0d12b4339c956313'
         '7170dedc9c87229ada0024e689ded642'
         '86d4a35722b5410e3b29fc92dae15d4b'
         'ce6c81ad1ad1f8b333fd6077d47abdaf'
         '3dc88030a8f2f5a5f97266d99b149f77'
         '7911a1f7bb30c171461a24fc55e227f0'
         'ceef8e36f98e45c3c7b9b8e7a37f89bf'
         'c23c73706a4f563ed7e109cebf18fa37'
         'cc008aa8bac19495524e40d3d5d3cb52'
         '77d7346c47e7239c6d4cb435bd649205'
         '2b61d704c4889b386db245cd3f5f577b'
         'fad5d2408a86deb2c97ad270fcc0ffb6'
         'f53826df7dd20ca39bff2c4fe3cf6bf9'
         '8e3ea1084f953a3c08111e8a85325514'
         '25245a7617e514b6dd73cbd6a30c37a6'
         '15d92ebc7786d9c4e9886ad4690dc7cc'
         '56d187ac985681c04448904ba21df49d'
         '36b7631011c803f51eab033b65ddc7f8'
         'ed2a55eabc50aa99999e75d852379c20'
         'd267d1e44b572cf46ec9b89a42be10c5'
         '0ce21faba49c0228bcbbef987b7c8900'
         'b76ef8dcc3b0be80c3f53ed3471d60c7'
         '4559dacfc74128e738dff901d935b596'
         '971e3f4a76543a8c7bdd31255b139e87'
         'a5f25338e5823d1dc56673f2585a2c30'
         '042e4154e827cf41e7bd8d9a6a502b0b'
         'a37cbb488c3c79a48300ba2fa28d56e8'
         '1bb896543bc36c3effa59152a6bb01a0'
         '3425f66e533edd5f9b023737c52f8ad6'
         '6b6405fd1f4d07c32515077bc5dd1ba1'
         'c9d5142093be0b4a3bd0802354c76089'
         'faec1a95ba6d592742e3e3244572f73b'
         'ead7e1a51efbeb7f403815761772290d'
         '2f7934bc35b629cd26a52d832354887f'
         'f6220602ca5d6f42683dd3a2733aacbd'
         '151cf7c9d9ef5a9e6281d59a1e456de2'
         '488b9103b347bc2f159c713580f309da'
         'd025ba6f149a34a0f4b7016c1d34af35'
         'e487cdf7a5b19e4aaec2a52c31b99d5e'
         '4528d85f7ea73a0964da1f1ac63af979'
         '09c6cbdea1f4bf9c9e6c1e5a0d9f7656'
         '62893a3f272cbe014225923d2d01bfc9'
         '945ad25982cc36ff1a0886f050208970'
         'd9baf1c284b184c7ffa4e02354447edd'
         'c4e8b53bdce575c1755c57acf0be18ea'
         '37af912b5618d474bb516650ac06bd0f'
         'a2c54619d4a3cf539485173568554e19'
         '9c91de23cbb2410aed7013d52fcc519e'
         '5ddbe9a89432258c50f450c5a1abf2da'
         'da1b8343854b284a3adca8c97aaa44a8'
         '46595b251844dc4d93e2111e552ef140'
         '8d2a17e265c6e83a2293a8f499127696'
         'f60ae3ef9198b1a5332e1d7687995c3f'
         'f2ba675d6efb586e7af9952116d17db7'
         '6a8ce0fe5e554254e8935deaf64d256d'
         '2d714a9dca1635f335275f7a9fb1ecec'
         'a908f3b36150e5de69fdab1e433b3f0b'
         '54105b20e250ee53fe5b7d640dfbf907'
         '71ba06492d8307b637dad6e26f97b11e'
         'd11f522d7aaa8b758e88a283784e8e16'
         '5a2d6a9ccf6e0f4253376bd137318acd'
         '2fb8764f74e1b1c3467bce15d63f4d67'
         '78ade086c16417684a81e71c0a6f8052'
         '760aa7152418d0fb39ee6c25ab3b9ec5'
         'a4214020828ee3ae1eecc32fafaecfb6'
         'b1c5ea329cace25c37e7de074d201360'
         '26531cf1402792673b173e4a381ebcd6'
         'b3b31cb6ed85bbfd768fd12ec6b06f77'
         '971762dbea9d2812dbe39681a33a78e4'
         '68e316dcbd16d5d2d106e24b76b81f59'
         '61c46ad71ee982af109f8d9cc80d5886'
         '2a061c7f8b6c66bb64a5b227619adf3c'
         'b6d7d1abc37c542871c2580859e49753'
         'c78bf349331f51829913594d9d1fbe0a'
         'f4c97210987e7076a3442f3135a5f2bc'
         '5ed46be5fe1bca49836b8523153bb248'
         '5c50db3f0888d80ecc2be4351879b1f6'
         'e4d32fa4336b46524597a3bbc715d272'
         'fb4979a32301f8dd1cc4ebdffd31cd10')

prepare() {
  apply_patches() {
      local PATCH
      for PATCH in "${source[@]}"; do
          PATCH="${PATCH%%::*}"
          PATCH="${PATCH##*/}"
          [[ ${PATCH} = $1*.patch ]] || continue
          msg2 "Applying patch: ${PATCH}..."
          patch -N -p1 < "../${PATCH}"
      done
  }

  cd ${_srcname}


  # Assorted LE ARM patches
  apply_patches 1

  # Assorted Manjaro ARM patches
  apply_patches 2
  
  # Assorted patches
  #  apply_patches 3

  
  cat "${srcdir}/config" > ./.config

  # add pkgrel to extraversion
  sed -ri "s|^(EXTRAVERSION =)(.*)|\1 \2-${pkgrel}|" Makefile

  # don't run depmod on 'make install'. We'll do this ourselves in packaging
  sed -i '2iexit 0' scripts/depmod.sh
  # make menuconfig
  # cp ./.config "${srcdir}/config"

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
  replaces=('linux-armv8' 'linux-aarch64' 'linux-khadas')
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
  replaces=('linux-aarch64-headers' 'linux-khadas')

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
