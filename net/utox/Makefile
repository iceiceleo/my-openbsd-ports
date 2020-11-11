# $OpenBSD: Makefile,v 1.7 2020/04/05 09:45:30 ajacoutot Exp $

COMMENT =	lightweight Tox client

V =		0.17.2

DISTNAME =	uTox-${V}-full
PKGNAME =	utox-${V}
MASTER_SITES =	https://github.com/uTox/uTox/releases/download/v${V}/

CATEGORIES =	net

HOMEPAGE =	https://utox.io

# MIT
PERMIT_PACKAGE =	Yes

WANTLIB += ICE SM X11 Xext Xrender c dbus-1 fontconfig freetype m pthread
WANTLIB += openal opus sodium toxcore v4lconvert vpx

MODULES =	devel/cmake

BUILD_DEPENDS =	devel/check

RUN_DEPENDS =	devel/desktop-file-utils

LIB_DEPENDS +=	audio/openal \
		multimedia/libv4l \
		net/toxcore \
		x11/dbus

COMPILER =	base-clang ports-gcc

NO_TEST =	yes

WRKDIST =	${WRKDIR}/uTox

CONFIGURE_ARGS =-DLLD_EMUL:String=${LLD_EMUL} \
		-DENABLE_FILTERAUDIO=OFF

post-extract:
	perl -i -pe 's/\r$$//' ${WRKSRC}/src/av/audio.h

.include <bsd.port.mk>
