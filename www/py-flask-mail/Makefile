# $NetBSD: Makefile,v 1.7 2019/07/09 23:02:29 nia Exp $

DISTNAME=	Flask-Mail-0.9.1
PKGNAME=	${PYPKGPREFIX}-${DISTNAME:tl}
CATEGORIES=	www python
MASTER_SITES=	${MASTER_SITE_PYPI:=F/Flask-Mail/}

MAINTAINER=	kleink@NetBSD.org
HOMEPAGE=	https://pythonhosted.org/Flask-Mail/
COMMENT=	Flask extension for sending email
LICENSE=	modified-bsd

USE_LANGUAGES=	# empty

DEPENDS+=	${PYPKGPREFIX}-blinker-[0-9]*:../../devel/py-blinker
DEPENDS+=	${PYPKGPREFIX}-flask-[0-9]*:../../www/py-flask

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
