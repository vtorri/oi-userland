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
# Copyright 2016 phorcys@126.com.  All rights reserved.
#

BUILD_STYLE=configure
BUILD_BITS=32_and_64
include ../../../make-rules/shared-macros.mk

COMPONENT_NAME=         libnfs
COMPONENT_VERSION=      1.9.8
COMPONENT_REVISION=     1
COMPONENT_FMRI=         library/libnfs
COMPONENT_CLASSIFICATION=System/Libraries
COMPONENT_PROJECT_URL=  https://github.com/sahlberg/libnfs/
COMPONENT_SUMMARY=      LIBNFS is a client library for accessing NFS shares over a network.
COMPONENT_SRC=          $(COMPONENT_NAME)-$(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=      $(COMPONENT_NAME)-$(COMPONENT_VERSION).tar.gz
COMPONENT_ARCHIVE_HASH= \
	sha256:e95af693e763a504eee72dacf3dc6c1001d83e40b807e7e1d0be2eaf48af779c
COMPONENT_ARCHIVE_URL=  \
	https://github.com/sahlberg/libnfs/archive/$(COMPONENT_ARCHIVE)
COMPONENT_LICENSE=      LGPLv2.1,BSD

TEST_TARGET=$(NO_TESTS)
include $(WS_MAKE_RULES)/common.mk

COMPONENT_PREP_ACTION= \
    ( cd  $(@D) && NOCONFIGURE=true sh bootstrap  )

CONFIGURE_OPTIONS+= --disable-static

# Auto-generated dependencies
REQUIRED_PACKAGES += system/library
