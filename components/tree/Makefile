#
# CDDL HEADER START
#
# The contents of this file are subject to the terms of the
# Common Development and Distribution License (the "License").
# You may not use this file except in compliance with the License.
#
# You can obtain a copy of the license at usr/src/OPENSOLARIS.LICENSE
# or http://www.opensolaris.org/os/licensing.
# See the License for the specific language governing permissions
# and limitations under the License.
#
# When distributing Covered Code, include this CDDL HEADER in each
# file and include the License file at usr/src/OPENSOLARIS.LICENSE.
# If applicable, add the following below this CDDL HEADER, with the
# fields enclosed by brackets "[]" replaced with your own identifying
# information: Portions Copyright [yyyy] [name of copyright owner]
#
# CDDL HEADER END
#

#
# Copyright (c) 2014, 2017, Oracle and/or its affiliates. All rights reserved.
#
BUILD_BITS= 64
include ../../make-rules/shared-macros.mk

COMPONENT_NAME=		tree
COMPONENT_VERSION=	1.7.0
COMPONENT_ARCHIVE=	$(COMPONENT_SRC).tgz
COMPONENT_ARCHIVE_HASH=	\
    sha256:6957c20e82561ac4231638996e74f4cfa4e6faabc5a2f511f0b4e3940e8f7b12
COMPONENT_PROJECT_URL=	http://mama.indstate.edu/users/ice/tree/
COMPONENT_ARCHIVE_URL=	$(COMPONENT_PROJECT_URL)src/$(COMPONENT_ARCHIVE)
COMPONENT_ANITYA_ID=	5006

TPNO=			27186

BUILD_STYLE= justmake
TEST_TARGET= $(NO_TESTS)
include $(WS_MAKE_RULES)/common.mk

# Fixes creation of executable
LDFLAGS += $(CC_BITS)

# The native Makefile invites patching to build for Solaris, but doing it here
# instead will keep it working if the build system changes.
COMPONENT_BUILD_ARGS += CC="$(CC)"
COMPONENT_BUILD_ARGS += CFLAGS="$(CFLAGS)"
COMPONENT_BUILD_ARGS += LDFLAGS="$(LDFLAGS)"
COMPONENT_INSTALL_ARGS += BINDIR=$(PROTOUSRBINDIR)
COMPONENT_INSTALL_ARGS += MANDIR=$(PROTOUSRSHAREMAN1DIR)
