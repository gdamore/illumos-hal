#
# This file and its contents are supplied under the terms of the
# Common Development and Distribution License ("CDDL"), version 1.0.
# You may only use this file in accordance with the terms of version
# 1.0 of the CDDL.
#
# A full copy of the text of the CDDL should have accompanied this
# source.  A copy of the CDDL is also available via the Internet
# at http://www.illumos.org/license/CDDL.
#

#
# Copyright 2011, Richard Lowe
# Copyright (c) 2012, Joyent, Inc.  All rights reserved.
# Copyright 2013 Nexenta Systems, Inc.  All rights reserved.
# Copyright 2014 Garrett D'Amore <garrett@damore.org>
#

include		$(SRC)//Makefile.master

MANSECT=	1m

_MANFILES=	\
		hal-device.1m		\
		hal-fdi-validate.1m	\
		hal-find.1m		\
		hal-get-property.1m	\
		hald.1m			\
		polkit-is-privileged.1m \
		rmmount.1m		\
		rmvolmgr.1m

i386_MANFILES=

sparc_MANFILES=

MANLINKS=	\
		hal-find-by-capability.1m	\
		hal-find-by-property.1m		\
		hal-set-property.1m

MANFILES=	$(_MANFILES) $($(MACH)_MANFILES)

hal-find-by-capability.1m	:= LINKSRC = hal-find.1m
hal-find-by-property.1m		:= LINKSRC = hal-find.1m

hal-set-property.1m		:= LINKSRC = hal-get-property.1m

.KEEP_STATE:

include		$(SRC)/man/Makefile.man

install:	$(ROOTMANFILES) $(ROOTMANLINKS)
