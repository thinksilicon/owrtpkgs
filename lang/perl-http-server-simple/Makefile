#
# Copyright (C) 2018 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=perl-http-server-simple
PKG_VERSION:=0.52
PKG_RELEASE:=1

PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/B/BP/BPS/
PKG_SOURCE:=HTTP-Server-Simple-$(PKG_VERSION).tar.gz
PKG_HASH:=d8939fa4f12bd6b8c043537fd0bf96b055ac3686b9cdd9fa773dca6ae679cb4c

PKG_LICENSE:=perl_5
PKG_MAINTAINER:=Moritz Meintker <git@thinksilicon.de>

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/HTTP-Server-Simple-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include ../perl/perlmod.mk

define Package/perl-exporter-tiny
  SUBMENU:=Perl
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=This is a simple standalone HTTP server.
  URL:=https://metacpan.org/pod/HTTP::Server::Simple
  DEPENDS:=perl +perlbase-autoloader +perlbase-config +perlbase-essential +perlbase-fcntl +perlbase-file +perlbase-getopt +perlbase-test
endef

define Build/Configure
        $(call perlmod/Configure,,)
endef

define Build/Compile
        $(call perlmod/Compile,,)
endef

define Package/perl-http-server-simple/install
        $(call perlmod/Install,$(1),Simple)
endef


$(eval $(call BuildPackage,perl-http-server-simple))

