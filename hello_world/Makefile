include $(TOPDIR)/rules.mk

PKG_NAME:=hello-world
PKG_VERSION:=1.0.1
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/shivshastha/new_source.git
PKG_SOURCE_VERSION:=ec0294a01995f5354ed5aaf3080d9aa93a91335c
PKG_SOURCE_DATE:=15-4-24


PKG_MAINTAINER:=Shiv Shastha <shivshastha.p@zilogic.com>

include $(INCLUDE_DIR)/package.mk

define Package/hello-world
  SECTION:=mypkg
  CATEGORY:=Basic
  TITLE:=Hello-world 
endef

define Package/world-world/description
  A simple Hello World! program.
endef

define Build/Compile
		$(MAKE) -C $(PKG_BUILD_DIR)/ \
			CC="$(TARGET_CC)"
endef

define Package/hello-world/install
	$(INSTALL_DIR) $(1)/usr/shiv
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/hello $(1)/usr/shiv
endef

$(eval $(call BuildPackage,hello-world))
