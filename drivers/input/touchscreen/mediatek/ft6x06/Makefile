include $(srctree)/drivers/misc/mediatek/Makefile.custom

ifeq ($(CONFIG_MTK_LCM_PHYSICAL_ROTATION), "90")
ccflags-y += -DMTK_LCM_PHYSICAL_ROTATION=\"90\"
endif

ifeq ($(CONFIG_MTK_LCM_PHYSICAL_ROTATION), "270")
ccflags-y += -DMTK_LCM_PHYSICAL_ROTATION=\"270\"
endif

ifeq ($(CONFIG_MTK_LCM_PHYSICAL_ROTATION), "180")
ccflags-y += -DMTK_LCM_PHYSICAL_ROTATION=\"180\"
endif

#ccflags-y += -I$(MTK_CUSTOM_PATH)/touchpanel/$(MTK_PLATFORM)/$(ARCH_MTK_PROJECT)/ft6x06/
#ccflags-y += -I$(MTK_CUSTOM_PATH)/touchpanel/

ccflags-y += -I$(MTK_PROJECT_PATH_ROOT)/touchpanel/ft6x06/

# Linux driver folder
#ccflags-y += -I$(srctree)/drivers/input/touchscreen/mediatek/$(MTK_PLATFORM)/$(ARCH_MTK_PROJECT)/ft6x06/
ccflags-y += -I$(srctree)/drivers/input/touchscreen/mediatek/
ccflags-y += -I$(srctree)/arch/arm/mach-$(MTK_PLATFORM)/$(ARCH_MTK_PROJECT)/touchpanel/ft6x06


ifeq ($(CONFIG_MTK_PLATFORM),"mt6572")
    ccflags-y += -DMT6572
endif

obj-y  +=  focaltech_ctl.o
obj-y  +=  ft6x06_button.o
obj-y  +=  ft6x06_driver.o
obj-y  +=  ft6x06_iic_wrap.o
obj-y  +=  ft6x06_isp.o
