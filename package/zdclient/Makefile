include $(TOPDIR)/rules.mk
	PKG_NAME:=zdclient
	PKG_RELEASE:=1
	PKG_BUILD_DIR := $(BUILD_DIR)/$(PKG_NAME)
include $(INCLUDE_DIR)/package.mk


define Package/zdclient
	SECTION:=net
	CATEGORY:=Network
	SUBMENU:=CERNET
	DEPENDS:=+libpcap
	TITLE:=zdclient ¡ª prints a snarky message
endef

define Package/zdclient/description
If you can¡¯t figure out what this program does, you¡¯re probably
brain-dead and need immediate medical attention.
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
	$(CP) ./src/* $(PKG_BUILD_DIR)/
endef

define Package/zdclient/install
	$(INSTALL_DIR) $(1)/usr/sbin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/zdclient $(1)/usr/sbin/
endef
$(eval $(call BuildPackage,zdclient))
