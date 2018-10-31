#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=liberation-fonts-ttf
PKG_VERSION:=2.00.1
PKG_RELEASE:=1
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://releases.pagure.org/liberation-fonts/
PKG_MD5SUM:=7890278A6CD17873C57D9CD785C2D230D9ABDEA837E96516019C5885DD271504

include $(INCLUDE_DIR)/package.mk

define Package/liberation-fonts
  SECTION:=fonts
  CATEGORY:=Network
  TITLE:=liberation-fonts
  SUBMENU:=Printing
  DEPENDS:= +fontconfig
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

define Package/liberation-fonts/postinst
#!/bin/sh
/usr/bin/fc-cache --force --verbose
endef

$(eval $(call BuildPackage,liberation-fonts))
