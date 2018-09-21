#
# Copyright (C) 2018 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=perl-sys-sigaction
PKG_VERSION:=0.23
PKG_RELEASE:=1

PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/L/LB/LBAXTER/
PKG_SOURCE:=Sys-SigAction-$(PKG_VERSION).tar.gz
PKG_HASH:=c4ef6c9345534031fcbbe2adc347fc7194d47afc945e7a44fac7e9563095d353

PKG_LICENSE:=perl_5
PKG_MAINTAINER:=Moritz Meintker <git@thinksilicon.de>

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Sys-SigAction-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include ../perl/perlmod.mk

define Package/perl-sys-sigaction
  SUBMENU:=Perl
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=Perl extension for Consistent Signal Handling
  URL:=https://metacpan.org/pod/Sys::SigAction
  DEPENDS:=perl +perlbase-autoloader +perlbase-config +perlbase-essential +perlbase-fcntl +perlbase-file +perlbase-getopt +perlbase-test
endef

define Build/Configure
        $(call perlmod/Configure,,)
endef

define Build/Compile
        $(call perlmod/Compile,,)
endef

define Package/perl-sys-sigaction/install
        $(call perlmod/Install,$(1),Sys auto/Sys/SigAction)
endef


$(eval $(call BuildPackage,perl-sys-sigaction))

