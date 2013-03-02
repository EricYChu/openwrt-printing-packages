#
# Copyright (C) 2013 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=liberation-fonts-ttf
PKG_VERSION:=2.00.1
PKG_RELEASE:=1
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://fedorahosted.org/releases/l/i/liberation-fonts/
PKG_MD5SUM:=5c781723a0d9ed6188960defba8e91cf

include $(INCLUDE_DIR)/package.mk

#PKG_UNPACK:=gzip -dc $(DL_DIR)/$(PKG_SOURCE) | $(TAR) -C $(PKG_BUILD_DIR) $(TAR_OPTIONS)

define Package/liberation-fonts
  SECTION:=fonts
  CATEGORY:=Network
  TITLE:=liberation-fonts
  SUBMENU:=Printing
endef

define Package/liberation-fonts/description
The Liberation(tm) Fonts is a font family which aims at metric compatibility
with Arial, Times New Roman, and Courier New. It is sponsored by Red Hat
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/liberation-fonts/install
	$(INSTALL_DIR) $(1)/usr/share/fonts/truetype/liberation
	$(CP) $(PKG_BUILD_DIR)/*.ttf $(1)/usr/share/fonts/truetype/liberation
endef

$(eval $(call BuildPackage,liberation-fonts))