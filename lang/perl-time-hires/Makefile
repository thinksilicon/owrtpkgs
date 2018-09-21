#
# Copyright (C) 2018 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=perl-time-hires
PKG_VERSION:=1.9758
PKG_RELEASE:=1

PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/J/JH/JHI/
PKG_SOURCE:=Time-HiRes-$(PKG_VERSION).tar.gz
PKG_HASH:=5bfa145bc11e70a8e337543b1084a293743a690691b568493455dedf58f34b1e

PKG_LICENSE:=perl_5
PKG_MAINTAINER:=Moritz Meintker <git@thinksilicon.de>

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Time-HighRes-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include ../perl/perlmod.mk

define Package/perl-time-highres
  SUBMENU:=Perl
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=High resolution alarm, sleep, gettimeofday, interval timers
  URL:=https://metacpan.org/pod/Time::HiRes
  DEPENDS:=perl +perlbase-autoloader +perlbase-config +perlbase-essential +perlbase-fcntl +perlbase-file +perlbase-getopt +perlbase-test
endef

define Build/Configure
        $(call perlmod/Configure,,)
endef

define Build/Compile
        $(call perlmod/Compile,,)
endef

define Package/perl-time-hires/install
        $(call perlmod/Install,$(1),Time auto/Time/HiRes)
endef


$(eval $(call BuildPackage,perl-acme-damn))

