#
# This file and its contents are supplied under the terms of the
# Common Development and Distribution License ("CDDL"), version 1.0.
# You may only use this file in accordance with the terms of version
# 1.0 of the CDDL.
#
# A full copy of the text of the CDDL should have accompanied this
# source.  A copy of the CDDL is also available via the Internet at
# http://www.illumos.org/license/CDDL.
#

#
# Copyright 2014 Alexander Pyhalov.  All rights reserved.
#

BUILD_BITS= 32_and_64
include ../../../make-rules/shared-macros.mk

COMPONENT_NAME= gnonlin
COMPONENT_VERSION= 0.10.17
COMPONENT_REVISION= 1
COMPONENT_SUMMARY= Non-linear editing elements for GStreamer
COMPONENT_SRC= $(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE= $(COMPONENT_SRC).tar.bz2
COMPONENT_PROJECT_URL = https://gstreamer.freedesktop.org
COMPONENT_ARCHIVE_URL=	$(COMPONENT_PROJECT_URL)/src/$(COMPONENT_NAME)/$(COMPONENT_ARCHIVE)
COMPONENT_ARCHIVE_HASH= sha256:e4a2dd8af1c0c97f2f63e918a25c26e871c896e88b7ee85948509f68f29e8935
COMPONENT_FMRI= library/audio/gstreamer/plugin/gnonlin
COMPONENT_CLASSIFICATION= System/Multimedia Libraries
COMPONENT_LICENSE= GPLv2, LGPLv2

include $(WS_MAKE_RULES)/common.mk

gcc_OPT= -O2

PATH= $(PATH.gnu)

# Documentation generation has changed
CONFIGURE_OPTIONS += --disable-gtk-doc

# CFLAGS are not passed to compiler when g-ir-scanner is used
COMPONENT_BUILD_ENV += CFLAGS="$(CFLAGS)"
COMPONENT_INSTALL_ENV += CFLAGS="$(CFLAGS)"

# Auto-generated dependencies
REQUIRED_PACKAGES += library/audio/gstreamer
REQUIRED_PACKAGES += library/glib2
REQUIRED_PACKAGES += system/library
