#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=svox
PKG_VERSION:=1.0+git20130326
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)_$(PKG_VERSION).orig.tar.gz
PKG_SOURCE_URL:=http://ftp.debian.org/debian/pool/non-free/s/svox
PKG_MD5SUM:=df4bf610ff4273b420e80ff64af93130

PKG_MAINTAINER:=Alessandro Di Marco <dmr@ethzero.com>
PKG_LICENSE:=Apache-2.0
PKG_LICENSE_FILES:=

PKG_FIXUP:=autoreconf
PKG_INSTALL:=1

include $(INCLUDE_DIR)/package.mk

define Package/svox
  TITLE:=SVOX PicoTTS text-to-speech engine
  SECTION:=sound
  CATEGORY:=Sound
  URL:=https://android.googlesource.com/platform/external/svox/
  DEPENDS:=+libpopt
endef

define Package/svox/description
  SVOX is an embedded speech technology company founded in 2000 and
  headquartered in Zurich, Switzerland. SVOX was acquired by Nuance
  Communications in 2011. Company's products included Automated Speech
  Recognition (ASR), Text-to-Speech (TTS) and Speech Dialog systems,
  with customers mostly being manufacturers and system integrators in
  automotive and mobile device industries.
  SVOX TTS technology is characterized by natural and clear sound as well
  as unique polyglot capability - the same voice can speak multiple
  languages like a native speaker.
endef

define Build/Prepare
	$(call Build/Prepare/Default)
	mv $(PKG_BUILD_DIR)/pico/* $(PKG_BUILD_DIR)
endef

define Build/Configure
	$(call Build/Configure/Default)
endef

define Package/svox/install
	$(call Build/Install/Default)
endef

$(eval $(call BuildPackage,svox))
