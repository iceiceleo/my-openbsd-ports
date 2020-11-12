# $OpenBSD: Makefile.template,v 1.88 2020/05/15 01:32:48 abieber Exp $

COMMENT =	rio-like Window Manager for Arcan

DISTNAME =	prio-20180913

GH_ACCOUNT =	letoram
GH_PROJECT =	prio
GH_COMMIT =	c3f97491339d15f063d6937d5f89bcfaea774dd1

CATEGORIES =	graphics plan9

#MAINTAINER =		???

# BSD
PERMIT_PACKAGE =	Yes

RUN_DEPENDS =		graphics/arcan

NO_BUILD =		Yes
NO_TEST =		Yes
PKG_ArCH =		*

do-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/arcan/
	${INSTALL_DATA_DIR} ${PREFIX}/share/arcan/appl/
	/bin/cp -R ${WRKDIST} ${PREFIX}/share/arcan/appl/prio
	/bin/ln -s ${LOCALBASE}/share/arcan/data/distr/launch \
		${PREFIX}/bin/prio

.include <bsd.port.mk>
