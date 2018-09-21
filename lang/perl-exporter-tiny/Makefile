#
# Copyright (C) 2018 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=perl-exporter-tiny
PKG_VERSION:=1.002001
PKG_RELEASE:=1

PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/T/TO/TOBYINK/
PKG_SOURCE:=Exporter-Tiny-$(PKG_VERSION).tar.gz
PKG_HASH:=a82c334c02ce4b0f9ea77c67bf77738f76a9b8aa4bae5c7209d1c76453d3c48d

PKG_LICENSE:=perl_5
PKG_MAINTAINER:=Moritz Meintker <git@thinksilicon.de>

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Exporter-Tiny-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include ../perl/perlmod.mk

define Package/perl-exporter-tiny
  SUBMENU:=Perl
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=an exporter with the features of Sub::Exporter but only core dependencies
  URL:=https://metacpan.org/pod/Exporter::Tiny
  DEPENDS:=perl +perlbase-autoloader +perlbase-config +perlbase-essential +perlbase-fcntl +perlbase-file +perlbase-getopt +perlbase-test
endef

define Build/Configure
        $(call perlmod/Configure,,)
endef

define Build/Compile
        $(call perlmod/Compile,,)
endef

define Package/perl-exporter-tiny/install
        $(call perlmod/Install,$(1),Exporter auto/Exporter/Tiny)
endef


$(eval $(call BuildPackage,perl-exporter-tiny))

