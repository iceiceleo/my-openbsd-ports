# $OpenBSD: Makefile.template,v 1.88 2020/05/15 01:32:48 abieber Exp $

COMMENT =	simple Wayland tiling window manager

DISTNAME =	velox-0.0.0.20201109

GH_ACCOUNT =	michaelforney
GH_PROJECT =	velox
GH_COMMIT =	2ae5e99dfcccfc10f98b3e1a697201db4a8676f8

CATEGORIES =	graphics

#MAINTAINER =		???

# ISC
PERMIT_PACKAGE =	Yes

#WANTLIB =		???

LIB_DEPENDS =		graphics/swc

MAKE_FLAGS +=		CC="${CC}" CFLAGS="${CFLAGS}"

USE_GMAKE =	Yes

# if debug packages are a good idea, extra configure args may be necessary
# and DEBUG_PACKAGES will commonly be set to ${BUILD_PACKAGES}
# DEBUG_CONFIGURE_ARGS =	???
# DEBUG_PACKAGES = ${BUILD_PACKAGES}

.include <bsd.port.mk>
