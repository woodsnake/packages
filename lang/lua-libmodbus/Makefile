include $(TOPDIR)/rules.mk

PKG_NAME:=lua-libmodbus
PKG_VERSION:=0.7.b
PKG_RELEASE:=1

PKG_SOURCE:=v$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/woodsnake/$(PKG_NAME)/archive/refs/tags
PKG_HASH:=00af4f5bfbb63a2df8a2b6a9dc6699822319c2e24c6dedd73321b72e32f3743a


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
