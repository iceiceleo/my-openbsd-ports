# $OpenBSD$

COMMENT =		Display server protocol
DISTNAME =		wayland-1.18.0

SHARED_LIBS =		wayland-client		0.0 # 3.0
SHARED_LIBS +=		wayland-cursor		0.0 # 0.0
SHARED_LIBS +=		wayland-egl		0.0 # 1.0
SHARED_LIBS +=		wayland-server		0.0 # 1.0

CATEGORIES =		graphics
HOMEPAGE =		https://wayland.freedesktop.org/
MAINTAINER =		Vadim Zhukov <persgray@gmail.com>

# MIT, examples (not packaged) are GPL
PERMIT_PACKAGE =	Yes

WANTLIB =		c expat ffi xml2

MASTER_SITES =		https://wayland.freedesktop.org/releases/
EXTRACT_SUFX =		.tar.xz

MODULES =		devel/meson

BUILD_DEPENDS =		textproc/libxslt

LIB_DEPENDS =		devel/libffi \
			textproc/libxml

CONFIGURE_ARGS =	-Ddocumentation=false
CFLAGS +=		-lkvm

.include <bsd.port.mk>
