#
# Copyright (C) 2018 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=perl-proc-daemon
PKG_VERSION:=0.23
PKG_RELEASE:=1

PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/A/AK/AKREAL/
PKG_SOURCE:=Proc-Daemon-$(PKG_VERSION).tar.gz
PKG_HASH:=34c0b85b7948b431cbabc97cee580835e515ccf43badbd8339eb109474089b69

PKG_LICENSE:=GNU_v1
PKG_MAINTAINER:=Moritz Meintker <git@thinksilicon.de>

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Proc-Daemon-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include ../perl/perlmod.mk

define Package/perl-proc-daemon
  SUBMENU:=Perl
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=Proc::Daemon - Run Perl program(s) as a daemon process.
  URL:=https://metacpan.org/pod/Proc::Daemon
  DEPENDS:=perl +perlbase-autoloader +perlbase-config +perlbase-essential +perlbase-fcntl +perlbase-file +perlbase-getopt +perlbase-test +perl-exporter-tiny
endef

define Build/Configure
        $(call perlmod/Configure,,)
endef

define Build/Compile
        $(call perlmod/Compile,,)
endef

define Package/perl-proc-daemon/install
        $(call perlmod/Install,$(1),Proc)
endef


$(eval $(call BuildPackage,perl-proc-daemon))

