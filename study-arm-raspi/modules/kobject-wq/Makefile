#CONFIG_MODULE_SIG=n
#CONFIG_MODULE_SIG_ALL=n

obj-m := kobject-wq.o

VER := v5.10
ARCH := arm
#ARCH := arm64
BOARD := pi3
#BOARD := pi4
BDO := def

ARCC := arm-linux-gnueabihf-
#ARCC := aarch64-linux-gnu-

BDIR := build-$(VER)-$(ARCH)-$(BOARD)-$(BDO)
KDIR := /home/raspi/Projects/kernel/build/$(BDIR)

MRUN := $(MAKE) ARCH=$(ARCH) CROSS_COMPILE=$(ARCC)

all: modules
modules:
	$(MRUN) -C $(KDIR) M=${shell pwd} modules

clean:
	$(MRUN) -C $(KDIR) M=${shell pwd} clean
