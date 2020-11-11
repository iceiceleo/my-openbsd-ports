# $OpenBSD: Makefile,v 1.21 2020/08/18 19:15:54 edd Exp $

COMMENT =	powerful display server and multimedia framework

SHARED_LIBS +=  arcan_a12                 0.0 # 0.1
SHARED_LIBS +=  arcan_shmif               0.0 # 0.13
SHARED_LIBS +=  arcan_shmif_ext           0.0 # 0.13
SHARED_LIBS +=  arcan_shmif_intext        0.0 # 0.13
SHARED_LIBS +=  arcan_shmif_server        0.0 # 0.13
SHARED_LIBS +=  arcan_tui                 0.0 # 0.13

DISTNAME =	arcan-0.6.0-pre3
GH_ACCOUNT =	iceiceleo
GH_PROJECT =	arcan
GH_COMMIT =	6b6e805a76e0e0622a40a5c02b9c7408aa99ce00

CATEGORIES =	graphics devel
HOMEPAGE =	https://arcan-fe.com

# TODO: bunch
PERMIT_PACKAGE =	Yes

WRKSRC =		${WRKDIST}/src

WANTLIB += ${COMPILER_LIBCXX} EGL GL avcodec avdevice avfilter
WANTLIB += avformat avutil bz2 c drm freetype gbm iconv luajit-5.1
WANTLIB += lzma m openal sqlite3 swresample swscale tesseract util
WANTLIB += vncclient vncserver wayland-server xcb xcb-composite
WANTLIB += xcb-icccm xcb-xfixes xkbcommon z

COMPILER =		base-clang ports-gcc base-gcc

MODULES =		devel/cmake

BUILD_DEPENDS =		graphics/wayland-protocols

LIB_DEPENDS =		archivers/bzip2 \
			audio/espeak \
			audio/openal \
			databases/sqlite3 \
			graphics/ffmpeg \
			graphics/tesseract/tesseract \
			graphics/wayland \
			lang/luajit \
			net/libvncserver \
			x11/xkbcommon

CONFIGURE_ARGS =	-DVIDEO_PLATFORM=egl-dri \
			-DHYBRID_HEADLESS=ON \
			-DDISABLE_FSRV_DECODE=ON # remove this to build with vlc

post-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/arcan/data/distr
	/bin/cp ${WRKDIST}/data/distr/launch \
		${PREFIX}/share/arcan/data/distr/
	sed -i'' 's,/usr/share/$$applname,${LOCALBASE}/share/arcan/appl,' \
		${PREFIX}/share/arcan/data/distr/launch

.include <bsd.port.mk>
