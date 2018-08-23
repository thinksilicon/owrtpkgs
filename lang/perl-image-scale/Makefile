#
# Copyright (C) 2018 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=perl-image-scale
PKG_VERSION:=0.14
PKG_RELEASE:=1

PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/A/AG/AGRUNDMA/
PKG_SOURCE:=Image-Scale-$(PKG_VERSION).tar.gz
PKG_HASH:=f09c5f0663b87738365ac2819e186b909abeb9ed85d83bc15ee76872c947cdf8

PKG_LICENSE:=GPL-2.0+
PKG_MAINTAINER:=Moritz Meintker <git@thinksilicon.de>

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Image-Scale-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include ../perl/perlmod.mk

define Package/perl-image-scale
  SUBMENU:=Perl
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=Fast, high-quality fixed-point image resizing
  URL:=https://metacpan.org/release/Image-Scale
  DEPENDS:=perl +perlbase-autoloader +perlbase-config +perlbase-essential +perlbase-fcntl +perlbase-file +perlbase-getopt +perlbase-test +perlbase-xsloader +libjpeg +libpng
endef

define Build/Configure
        $(call perlmod/Configure,,)
endef

define Build/Compile
        $(call perlmod/Compile,,)
endef

define Package/perl-image-scale/install
        $(call perlmod/Install,$(1),Image auto/Image)
endef


$(eval $(call BuildPackage,perl-image-scale))

