#########################################################
# Bluetooth character device driver
#########################################################

############ 7668 BT sdio Driver ########################
ifneq ($(filter "MT7668",$(CONFIG_MTK_COMBO_CHIP)),)
obj-m += btmtksdio.o
btmtksdio-objs     := btmtk_sdio.o btmtk_main.o
endif
