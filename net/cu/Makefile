#
# Copyright (C) 2018 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=cu
PKG_VERSION:=1.07
PKG_RELEASE:=1

PKG_SOURCE:=uucp-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=ftp://ftp.gnu.org/pub/gnu/uucp/
PKG_HASH:=060c15bfba6cfd1171ad81f782789032113e199a5aded8f8e0c1c5bd1385b62c

PKG_LICENSE:=GPLv2
PKG_MAINTAINER:=Moritz Meintker <git@thinksilicon.de>

include $(INCLUDE_DIR)/package.mk

define Package/cu
	SECTION:=net
	CATEGORY:=Network
	TITLE:=The cu command is used to call up another system and act as a dial-in terminal.
	URL:=https://airs.com/ian/uucp.html
endef

define define Package/cu/description
	The cu command is used to call up another system and act as a dial-in terminal (mostly on a serial line).
	It can also do simple file transfers with no error checking.

	cu is part of the UUCP source but has been split into its own package because it can be useful even if you do not do uucp. 
endef

define Build/Prepare
        $(PKG_UNPACK)
        cp -R $(PKG_BUILD_DIR)/../uucp-$(PKG_VERSION)/* $(PKG_BUILD_DIR)/
        rm -r $(PKG_BUILD_DIR)/../uucp-$(PKG_VERSION)
	$(Build/Patch)
endef


CONFIGURE_ARGS+= \
	--prefix=/usr \

define Package/cu/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/cu $(1)/usr/bin/
endef

$(eval $(call BuildPackage,cu))
