# $NetBSD: Makefile,v 1.32 2020/06/07 11:17:30 fcambus Exp $

DISTNAME=		yabasic-2.86.9
CATEGORIES=		lang
MASTER_SITES=		http://www.yabasic.de/download/

MAINTAINER=		pkgsrc-users@NetBSD.org
HOMEPAGE=		http://www.yabasic.de/
COMMENT=		Yet another Basic for Unix and Windows
LICENSE=		mit

GNU_CONFIGURE=		yes
USE_NCURSES=		yes
AUTO_MKDIRS=		yes

TEST_TARGET=		check

post-install:
	${INSTALL_DATA} ${WRKSRC}/yabasic.htm \
		${DESTDIR}${PREFIX}/share/doc/yabasic

BUILDLINK_DEPMETHOD.libXt?=	build

.include "../../devel/libffi/buildlink3.mk"
.include "../../devel/ncurses/buildlink3.mk"
.include "../../x11/libSM/buildlink3.mk"
.include "../../x11/libX11/buildlink3.mk"
.include "../../x11/libXt/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
