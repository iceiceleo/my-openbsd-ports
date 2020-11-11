# $OpenBSD: Makefile.template,v 1.88 2020/05/15 01:32:48 abieber Exp $

COMMENT =	small Wayland compositor implemented as a library

DISTNAME =	swc-0.0.0.20200915

GH_ACCOUNT =	michaelforney
GH_PROJECT =	swc
GH_COMMIT =	ab8130100e17b0e06c26b895151a7c9315a597e6

SHARED_LIBS =	swc	0.0

CATEGORIES =	graphics

#MAINTAINER =		???

# ISC
PERMIT_PACKAGE =	Yes

#WANTLIB =		???

BUILD_DEPENDS =		graphics/wayland-protocols
LIB_DEPENDS =		graphics/wayland \
					x11/xkbcommon

MAKE_FLAGS +=		CC="${CC}" CFLAGS="${CFLAGS}"

USE_GMAKE =	Yes

# if debug packages are a good idea, extra configure args may be necessary
# and DEBUG_PACKAGES will commonly be set to ${BUILD_PACKAGES}
# DEBUG_CONFIGURE_ARGS =	???
# DEBUG_PACKAGES = ${BUILD_PACKAGES}

.include <bsd.port.mk>
