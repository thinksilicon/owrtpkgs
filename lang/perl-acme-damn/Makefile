#
# Copyright (C) 2018 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=perl-acme-damn
PKG_VERSION:=0.08
PKG_RELEASE:=1

PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/I/IB/IBB/
PKG_SOURCE:=Acme-Damn-$(PKG_VERSION).tar.gz
PKG_HASH:=310d2d03ff912dcd42e4d946174099f41fe3a2dd57a497d6bd65baf1759b7e0e

PKG_LICENSE:=perl_5
PKG_MAINTAINER:=Moritz Meintker <git@thinksilicon.de>

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Acme-Damn-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include ../perl/perlmod.mk

define Package/perl-acme-damn
  SUBMENU:=Perl
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:='Unbless' Perl objects.
  URL:=https://metacpan.org/pod/Acme::Damn
  DEPENDS:=perl +perlbase-autoloader +perlbase-config +perlbase-essential +perlbase-fcntl +perlbase-file +perlbase-getopt +perlbase-test +perlbase-dynaloader
endef

define Build/Configure
        $(call perlmod/Configure,,)
endef

define Build/Compile
        $(call perlmod/Compile,,)
endef

define Package/perl-acme-damn/install
        $(call perlmod/Install,$(1),Acme auto/Acme/Damn)
endef


$(eval $(call BuildPackage,perl-acme-damn))

