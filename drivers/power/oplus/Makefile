gki_support =
ifeq ($(CONFIG_OPLUS_CHG),y)
gki_support = yes
endif
ifeq ($(CONFIG_OPLUS_CHG),m)
gki_support = yes
endif

ifdef gki_support

oplus_chg-y += oplus_debug_info.o
oplus_chg-y += oplus_charger.o
oplus_chg-y += oplus_gauge.o
oplus_chg-y += oplus_vooc.o
oplus_chg-y += oplus_pps.o
oplus_chg-y += oplus_adapter.o
oplus_chg-y += oplus_short.o
oplus_chg-y += oplus_wireless.o
oplus_chg-y += oplus_configfs.o
oplus_chg-y += oplus_chg_ops_manager.o
oplus_chg-y += adapter_ic/oplus_stm.o
oplus_chg-y += charger_ic/oplus_short_ic.o
oplus_chg-y += gauge_ic/oplus_bq27541.o
oplus_chg-y += vooc_ic/oplus_stm8s.o
oplus_chg-y += vooc_ic/oplus_n76e.o
oplus_chg-y += vooc_ic/oplus_rk826.o
oplus_chg-y += vooc_ic/oplus_op10.o
oplus_chg-y += vooc_ic/oplus_rt5125.o
oplus_chg-y += vooc_ic/oplus_vooc_fw.o
oplus_chg-y += voocphy/oplus_sc8547.o
oplus_chg-y += voocphy/oplus_sc8547_slave.o
ifneq ($(CONFIG_OPLUS_CHARGER_MTK),y)
oplus_chg-y += wireless_ic/oplus_p922x.o
oplus_chg-y += wireless_ic/oplus_nu1619.o
oplus_chg-y += wireless_ic/oplus_chargepump.o
endif

oplus_chg-$(CONFIG_OPLUS_SM8350_CHARGER) += charger_ic/oplus_battery_sm8350.o charger_ic/oplus_da9313.o charger_ic/oplus_mp2650.o voocphy/oplus_adsp_voocphy.o voocphy/oplus_voocphy.o

obj-$(CONFIG_OPLUS_CHG) := oplus_chg.o

else

ifeq ($(CONFIG_OPLUS_CHARGER_MTK),y)
subdir-ccflags-y += -Werror
subdir-ccflags-y += -Wno-unused-variable
ifeq ($(CONFIG_OPLUS_CHARGER_MTK6779Q),y)
subdir-ccflags-y += -I$(srctree)/drivers/misc/mediatek/include
endif
endif
ifeq ($(CONFIG_OPLUS_CHARGER_MTK6889),y)
subdir-ccflags-y += -I$(srctree)/drivers/misc/mediatek/include
endif
ifeq ($(CONFIG_OPLUS_CHARGER_MTK6893),y)
subdir-ccflags-y += -I$(srctree)/drivers/misc/mediatek/include
endif
ifeq ($(CONFIG_OPLUS_CHARGER_MTK6877),y)
subdir-ccflags-y += -I$(srctree)/drivers/misc/mediatek/include
subdir-ccflags-y += -Werror
subdir-ccflags-y += -Wunused
subdir-ccflags-y += -Wno-unused-result
endif
ifeq ($(CONFIG_OPLUS_CHARGER_MTK6779R),y)
subdir-ccflags-y += -I$(srctree)/drivers/misc/mediatek/include
endif
ifeq ($(CONFIG_OPLUS_CHARGER_MTK6765R),y)
subdir-ccflags-y += -I$(srctree)/drivers/misc/mediatek/include
endif
ifneq ($(CONFIG_OPLUS_CHARGER_MTK),y)
obj-y      += wireless_ic/
endif
obj-y      += charger_ic/
obj-y      += gauge_ic/
obj-y      += vooc_ic/
obj-y      += adapter_ic/

obj-y      += voocphy/

#obj-y   += oplus_voocphy.o

obj-y	+= oplus_charger.o
obj-y	+= oplus_gauge.o
obj-y	+= oplus_vooc.o
obj-y	+= oplus_adapter.o
obj-y	+= oplus_wireless.o
obj-y	+= oplus_short.o
obj-y   += oplus_debug_info.o
obj-y   += oplus_chg_ops_manager.o
obj-y	+= oplus_pps.o
obj-y   += oplus_configfs.o
endif

