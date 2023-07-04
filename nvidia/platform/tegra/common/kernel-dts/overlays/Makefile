old-dtbo := $(dtbo-y)
dtbo-y :=
makefile-path := platform/tegra/common/kernel-dts/overlays

BUILD_ENABLE=n
ifneq ($(filter y,$(CONFIG_ARCH_TEGRA_23x_SOC)),)
BUILD_ENABLE=y
endif

dtbo-$(BUILD_ENABLE) += jetson-mcp251x-overlay.dtbo

ifneq ($(dtbo-y),)
dtbo-y := $(addprefix $(makefile-path)/,$(dtbo-y))
endif

dtbo-y += $(old-dtbo)
