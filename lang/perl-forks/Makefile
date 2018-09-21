#
# Copyright (C) 2018 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=perl-forks
PKG_VERSION:=0.36
PKG_RELEASE:=1

PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/R/RY/RYBSKEJ/
PKG_SOURCE:=forks-$(PKG_VERSION).tar.gz
PKG_HASH:=61be24e44f4c6fea230e8354678beb5b7adcfefd909a47db8f0a251b0ab65993

PKG_LICENSE:=perl_5
PKG_MAINTAINER:=Moritz Meintker <git@thinksilicon.de>

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/forks-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include ../perl/perlmod.mk

define Package/perl-forks
  SUBMENU:=Perl
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=forks - drop-in replacement for Perl threads using fork()
  URL:=https://metacpan.org/pod/forks
  DEPENDS:=perl +perlbase-autoloader +perlbase-config +perlbase-essential +perlbase-fcntl +perlbase-file +perlbase-getopt +perlbase-test +perlbase-sigtrap +perlbase-storable +perl-list-moreutils +perl-sys-sigaction +perl-acme-damn
endef

define Build/Configure
        $(call perlmod/Configure,,)
endef

define Build/Compile
        $(call perlmod/Compile,,)
endef

define Package/perl-forks/install
        $(call perlmod/Install,$(1),forks.pm forks threads auto/forks)
endef


$(eval $(call BuildPackage,perl-forks))

