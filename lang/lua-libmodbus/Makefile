include $(TOPDIR)/rules.mk

PKG_NAME:=lua-libmodbus
PKG_VERSION:=0.7-1
PKG_RELEASE:=1

PKG_SOURCE:=v$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/woodsnake/$(PKG_NAME)/archive/refs/tags
PKG_HASH:=502e3b16e7ffec80247695c9a5f8d5ad12c287bf03f09dead47aa083b1d7ef26

PKG_MAINTAINER:=Karl Palsson <karlp@etactica.com>
PKG_LICENSE:=MIT

include $(INCLUDE_DIR)/package.mk

define Package/lua-libmodbus
  SUBMENU:=Lua
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=lua-libmodbus
  URL:=https://github.com/etactica/lua-libmodbus
  DEPENDS:=+liblua +libmodbus
endef

define Package/lua-libmodbus/description
	lua-libmodbus is a binding to libmodbus,
	see also http://www.libmodbus.org
endef

define Build/Configure
endef

define Package/lua-libmodbus/install
	$(INSTALL_DIR) $(1)/usr/lib/lua
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/libmodbus.so $(1)/usr/lib/lua
endef

$(eval $(call BuildPackage,lua-libmodbus))
