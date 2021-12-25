# Build all libraries

include ~/big/stm32f4/target/stm32f4discovery/gcc_conf.makefile
CFLAGS += -fno-strict-aliasing -fwrapv

FLOAT_TYPE = hard

all:
	$(MAKE) -C USB_OTG FLOAT_TYPE=$(FLOAT_TYPE)
	$(MAKE) -C USB_Device/Core FLOAT_TYPE=$(FLOAT_TYPE)
	$(MAKE) -C USB_Device/Class/cdc FLOAT_TYPE=$(FLOAT_TYPE)

clean:
	$(MAKE) clean -C USB_OTG
	$(MAKE) clean -C USB_Device/Core
	$(MAKE) clean -C USB_Device/Class/cdc
