#
# Copyright (C) 2015 MediaTek Inc.
#
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License version 2 as
# published by the Free Software Foundation.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
# GNU General Public License for more details.
#

#
# Makefile for Mediatek(R) MMC/SD host controller drivers
#

#add kernel source code path as head file search path
MTK_PLATFORM := $(subst ",,$(CONFIG_MTK_PLATFORM))
ccflags-y += -I$(srctree)/drivers/misc/mediatek/include
ccflags-y += -I$(srctree)/drivers/misc/mediatek/include/mt-plat/$(MTK_PLATFORM)/include
ccflags-y += -I$(srctree)/drivers/misc/mediatek/include/mt-plat
ccflags-y += -I$(srctree)/drivers/misc/mediatek/base/power/$(MTK_PLATFORM)
ccflags-y += -I$(srctree)/drivers/misc/mediatek/base/power/include
#obj-$(CONFIG_MMC_MTK_PRO) += $(subst ",,$(CONFIG_MTK_PLATFORM))/

ifeq ($(CONFIG_MTK_HW_FDE_AES),y)
ccflags-y += -I$(srctree)/drivers/misc/mediatek/fde_aes/$(MTK_PLATFORM)
endif

ifeq ($(CONFIG_TRUSTONIC_TEE_SUPPORT),y)
include $(srctree)/drivers/misc/mediatek/gud/Makefile.include
ccflags-y += -I$(srctree)/drivers/mmc/host/mediatek/rpmb/drrpmb/public
ccflags-y += -I$(srctree)/drivers/mmc/host/mediatek/rpmb/drrpmb_gp/public
ccflags-y += -I$(srctree)/drivers/mmc/host/mediatek/rpmb/tlrpmb/public
endif

ccflags-y += -I$(srctree)
#workaround for include mmc/card/queue.h and mmc/core/core.h
ccflags-y += -I$(srctree)/drivers


ifeq ($(CONFIG_MTK_PLATFORM), "mt6739")
ccflags-y += -I$(srctree)/drivers/mmc/host/mediatek/ComboA
ccflags-y += -I$(srctree)/drivers/mmc/host/mediatek/ComboA/mt6739
obj-$(CONFIG_MMC_MTK_PRO) += ComboA/

else ifeq ($(CONFIG_MTK_PLATFORM), "mt6799")
ccflags-y += -I$(srctree)/drivers/mmc/host/mediatek/ComboA
ccflags-y += -I$(srctree)/drivers/mmc/host/mediatek/ComboA/mt6799
obj-$(CONFIG_MMC_MTK_PRO) += ComboA/

else ifeq ($(CONFIG_MTK_PLATFORM), "mt6763")
ccflags-y += -I$(srctree)/drivers/mmc/host/mediatek/ComboA
ccflags-y += -I$(srctree)/drivers/mmc/host/mediatek/ComboA/mt6763
obj-$(CONFIG_MMC_MTK_PRO) += ComboA/

else ifeq ($(CONFIG_MTK_PLATFORM), "mt6771")
ccflags-y += -I$(srctree)/drivers/mmc/host/mediatek/ComboA
ccflags-y += -I$(srctree)/drivers/mmc/host/mediatek/ComboA/mt6771
obj-$(CONFIG_MMC_MTK_PRO) += ComboA/

else ifeq ($(CONFIG_MTK_PLATFORM), "mt6757")
ccflags-y += -I$(srctree)/drivers/mmc/host/mediatek/mt6757
ccflags-y += -I$(srctree)/drivers/mmc/host/mediatek/mt6757/mt6757
obj-$(CONFIG_MMC_MTK_PRO) += mt6757/

else ifeq ($(CONFIG_MTK_PLATFORM), "mt6758")
ccflags-y += -I$(srctree)/drivers/mmc/host/mediatek/mt6758
ccflags-y += -I$(srctree)/drivers/mmc/host/mediatek/mt6758/mt6758
obj-$(CONFIG_MMC_MTK_PRO) += mt6758/

else ifeq ($(CONFIG_MTK_PLATFORM), "mt6759")
ccflags-y += -I$(srctree)/drivers/mmc/host/mediatek/mt6759
ccflags-y += -I$(srctree)/drivers/mmc/host/mediatek/mt6759/mt6759
obj-$(CONFIG_MMC_MTK_PRO) += mt6759/

else ifeq ($(CONFIG_MTK_PLATFORM), "mt6775")
ccflags-y += -I$(srctree)/drivers/mmc/host/mediatek/mt6775
ccflags-y += -I$(srctree)/drivers/mmc/host/mediatek/mt6775/mt6775
obj-$(CONFIG_MMC_MTK_PRO) += mt6775/

else ifeq ($(CONFIG_MTK_PLATFORM), "mt8167")
ccflags-y += -I$(srctree)/drivers/mmc/host/mediatek/mt8167
obj-$(CONFIG_MMC_MTK_SDIO) += mt8167/

ccflags-y += -I$(srctree)/drivers/mmc/host/mediatek/$(MTK_PLATFORM)
obj-$(CONFIG_MMC_MTK_PRO) += $(subst ",,$(CONFIG_MTK_PLATFORM))/
endif
