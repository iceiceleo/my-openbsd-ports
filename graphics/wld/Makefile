# $OpenBSD: Makefile.template,v 1.88 2020/05/15 01:32:48 abieber Exp $

COMMENT =	primitive drawing library targeted at Wayland

DISTNAME =	wld-0.0.0.20200220

GH_ACCOUNT =	michaelforney
GH_PROJECT =	wld
GH_COMMIT =	ea4eccb64cfcfc508b029a530fc434d6e6695af5

SHARED_LIBS =	wld	0.0

CATEGORIES =	graphics

#MAINTAINER =		???

# ISC
PERMIT_PACKAGE =	Yes

#WANTLIB =		???

LIB_DEPENDS =		graphics/wayland

MAKE_FLAGS +=		CC="${CC}" CFLAGS="${CFLAGS}"

USE_GMAKE =	Yes

# if debug packages are a good idea, extra configure args may be necessary
# and DEBUG_PACKAGES will commonly be set to ${BUILD_PACKAGES}
# DEBUG_CONFIGURE_ARGS =	???
# DEBUG_PACKAGES = ${BUILD_PACKAGES}

.include <bsd.port.mk>
