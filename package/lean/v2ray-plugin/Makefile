#
<<<<<<< HEAD
# Copyright (C) 2018-2020 chenhw2 <https://github.com/chenhw2>
#
# This is free software, licensed under the GNU General Public License v3.
# See /LICENSE for more information.
#
#
=======
# Copyright (C) 2020 SharerMax
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

>>>>>>> c395eff6e974bd226c45cf5d70eccba4677f55c0
include $(TOPDIR)/rules.mk

PKG_NAME:=v2ray-plugin
PKG_VERSION:=1.3.0
<<<<<<< HEAD
PKG_RELEASE:=20200205
PKG_MAINTAINER:=chenhw2 <https://github.com/chenhw2>

# OpenWrt ARCH: arm, i386, x86_64, mips, mipsel
# Golang ARCH: arm[5-7], 386, amd64, mips, mipsle
PKG_ARCH:=$(ARCH)
BIN_ARCH:=$(ARCH)
ifeq ($(ARCH),mips)
    BIN_ARCH:=mips_sf
endif
ifeq ($(ARCH),mipsel)
	PKG_ARCH:=mips
	BIN_ARCH:=mipsle_sf
endif
ifeq ($(ARCH),i386)
	PKG_ARCH:=386
	BIN_ARCH:=386
endif
ifeq ($(ARCH),x86_64)
	PKG_ARCH:=amd64
	BIN_ARCH:=amd64
endif
ifeq ($(ARCH),arm)
	BIN_ARCH:=arm7
endif

PKG_SOURCE:=v2ray-plugin-linux-$(PKG_ARCH)-v$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/shadowsocks/v2ray-plugin/releases/download/v$(PKG_VERSION)/
PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)
PKG_HASH:=skip

include $(INCLUDE_DIR)/package.mk
=======
PKG_RELEASE:=1
PKG_MAINTAINER:=ShareMax
PKG_BUILD_DIR:=$(BUILD_DIR)/v2ray-plugin-$(PKG_VERSION)

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/shadowsocks/v2ray-plugin/tar.gz/v$(PKG_VERSION)?
PKG_HASH:=dfb86cd8d9be86e665c4b86b68cd7037e4310de001656eef01ec9aeea71edd10

PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE
PKG_MAINTAINER:=madeye <max.c.lv@gmail.com>

GO_PKG:=github.com/shadowsocks/v2ray-plugin


include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/golang/golang-package.mk

>>>>>>> c395eff6e974bd226c45cf5d70eccba4677f55c0

define Package/v2ray-plugin
	SECTION:=net
	CATEGORY:=Network
	TITLE:=SIP003 plugin for shadowsocks, based on v2ray
	URL:=https://github.com/shadowsocks/v2ray-plugin
<<<<<<< HEAD
=======
	DEPENDS:=$(GO_ARCH_DEPENDS) +ca-certificates
>>>>>>> c395eff6e974bd226c45cf5d70eccba4677f55c0
endef

define Package/v2ray-plugin/description
	Yet another SIP003 plugin for shadowsocks, based on v2ray
endef

define Build/Prepare
<<<<<<< HEAD
	gzip -dc "$(DL_DIR)/$(PKG_SOURCE)" | tar -C $(PKG_BUILD_DIR)/ -xf -
endef

define Build/Compile
	echo "$(PKG_NAME)Compile Skiped!"
=======
	$(call Build/Prepare/Default)
endef

define Build/Compile
	$(call GoPackage/Build/Compile)
>>>>>>> c395eff6e974bd226c45cf5d70eccba4677f55c0
endef

define Package/v2ray-plugin/install
	$(INSTALL_DIR) $(1)/usr/bin
<<<<<<< HEAD
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/v2ray-plugin_linux_$(BIN_ARCH) $(1)/usr/bin/v2ray-plugin
endef

=======
	$(INSTALL_BIN) $(GO_PKG_BUILD_BIN_DIR)/v2ray-plugin $(1)/usr/bin/v2ray-plugin
endef
$(eval $(call GoBinPackage,v2ray-plugin))
>>>>>>> c395eff6e974bd226c45cf5d70eccba4677f55c0
$(eval $(call BuildPackage,v2ray-plugin))
