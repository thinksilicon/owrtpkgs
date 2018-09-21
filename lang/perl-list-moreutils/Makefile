#
# Copyright (C) 2018 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=perl-list-moreuitls
PKG_VERSION:=0.428
PKG_RELEASE:=1

PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/R/RE/REHSACK/
PKG_SOURCE:=List-MoreUtils-$(PKG_VERSION).tar.gz
PKG_HASH:=713e0945d5f16e62d81d5f3da2b6a7b14a4ce439f6d3a7de74df1fd166476cc2

PKG_LICENSE:=apache_2_0
PKG_MAINTAINER:=Moritz Meintker <git@thinksilicon.de>

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/list-moreutils-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include ../perl/perlmod.mk

define Package/perl-forks
  SUBMENU:=Perl
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=List::MoreUtils - Provide the stuff missing in List::Util
  URL:=https://metacpan.org/pod/List::MoreUtils
  DEPENDS:=perl +perlbase-autoloader +perlbase-config +perlbase-essential +perlbase-fcntl +perlbase-file +perlbase-getopt +perlbase-test
endef

define Build/Configure
        $(call perlmod/Configure,,)
endef

define Build/Compile
        $(call perlmod/Compile,,)
endef

define Package/perl-list-moreutils/install
        $(call perlmod/Install,$(1),List auto/List)
endef


$(eval $(call BuildPackage,perl-list-moreutils))

