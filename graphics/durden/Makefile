# $OpenBSD: Makefile.template,v 1.88 2020/05/15 01:32:48 abieber Exp $

COMMENT =	Desktop Environment for Arcan

DISTNAME =	durden-0.6-pre2

GH_ACCOUNT =	letoram
GH_PROJECT =	durden
GH_COMMIT =	eee68051e22cdbb6ffcb4924b63a8eb61e105dc8

CATEGORIES =	graphics

# https preferred for HOMEPAGE
#MAINTAINER =		???

PERMIT_PACKAGE =	Yes

RUN_DEPENDS =		graphics/arcan

NO_BUILD =		Yes
NO_TEST =		Yes
PKG_ARCH =		*

do-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/arcan/
	${INSTALL_DATA_DIR} ${PREFIX}/share/arcan/appl/
	/bin/cp -R ${WRKDIST}/durden ${PREFIX}/share/arcan/appl/
	/bin/ln -s ${LOCALBASE}/share/arcan/data/distr/launch \
		${PREFIX}/bin/durden

.include <bsd.port.mk>
