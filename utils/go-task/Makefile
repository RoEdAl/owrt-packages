include $(TOPDIR)/rules.mk

PKG_NAME:=go-task
PKG_VERSION:=3.34.1
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_VERSION:=v3.34.1
PKG_SOURCE_URL:=http://github.com/go-task/task
PKG_MIRROR_HASH:=a828304bcde870ef2b33d08d32c5bbace71b85cc31e6bd352a4584b4e2d94f54

PKG_MAINTAINER:=
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=golang/host
PKG_BUILD_PARALLEL:=1
PKG_BUILD_FLAGS:=no-mips16

GO_PKG:=github.com/go-task/task/v3/cmd/task
GO_PKG_LDFLAGS_X:=$(GO_PKG)/cmd.Version=$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include ../../lang/golang/golang-package.mk

define Package/go-task
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=A simple task runner
  URL:=http://taskfile.dev
  DEPENDS:=$(GO_ARCH_DEPENDS)
endef

define Package/go-task/description
  A task runner / simpler Make alternative written in Go.
  Tasks are defined in a simple YAML file.
endef

$(eval $(call GoBinPackage,go-task))
$(eval $(call BuildPackage,go-task))
