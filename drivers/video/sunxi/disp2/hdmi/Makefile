obj-$(CONFIG_HDMI_DISP2_SUNXI) += hdmi.o

hdmi-y := drv_hdmi.o hdmi_core.o hdmi_edid.o
ifeq ($(CONFIG_ARM64),y)
hdmi-$(CONFIG_ARCH_SUN50IW1P1) += libhdmi_sun50iw1.o
hdmi-$(CONFIG_ARCH_SUN50IW2P1) += libhdmi_sun50iw1.o
endif

ifeq ($(CONFIG_ARM),y)
hdmi-$(CONFIG_ARCH_SUN50IW1P1) += libhdmi_sun8iw11.o
hdmi-$(CONFIG_ARCH_SUN50IW2P1) += libhdmi_sun8iw11.o
hdmi-$(CONFIG_ARCH_SUN8IW11)   += libhdmi_sun8iw11.o
endif

$(obj)/libhdmi_sun50iw1.o:
	cp $(srctree)/drivers/video/sunxi/disp2/hdmi/libhdmi_sun50iw1 $(obj)/libhdmi_sun50iw1.o
