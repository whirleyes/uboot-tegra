#
# Copyright (c) 2011 The Chromium OS Authors. All rights reserved.
# Use of this source code is governed by a BSD-style license that can be
# found in the LICENSE file.
#
# Alternatively, this software may be distributed under the terms of the
# GNU General Public License ("GPL") version 2 as published by the Free
# Software Foundation.
#

include $(TOPDIR)/config.mk

LIB	= $(obj)libvboot.a

COBJS-$(CONFIG_CHROMEOS_VBOOT) += boot_kernel.o
COBJS-$(CONFIG_CHROMEOS_VBOOT) += bootstub_entry.o
COBJS-$(CONFIG_CHROMEOS_VBOOT) += firmware_cache.o
COBJS-$(CONFIG_CHROMEOS_VBOOT) += global_data.o
COBJS-$(CONFIG_CHROMEOS_VBOOT) += main_entry.o

COBJS-$(CONFIG_CHROMEOS_TWOSTOP) += boot_kernel.o

COBJS	:= $(COBJS-y)
OBJS	:= $(addprefix $(obj),$(COBJS))

$(LIB):	$(obj).depend $(OBJS)
	$(AR) $(ARFLAGS) $@ $(OBJS)

#########################################################################

# defines $(obj).depend target
include $(SRCTREE)/rules.mk

sinclude $(obj).depend

#########################################################################
