# $NetBSD: Makefile,v 1.32 2020/05/19 13:58:24 joerg Exp $

PKGNAME=	gnuradio-doxygen-${VERSION}
PKGREVISION=	4
COMMENT=	Doxygen documentation of GNU Radio

BUILD_DIRS=	build/docs

.include	"../../ham/gnuradio-core/Makefile.common"
.include	"../../ham/gnuradio-core/Nocore.mk"

BUILD_DEPENDS+=	doxygen>=1.8.15:../../devel/doxygen
BUILD_DEPENDS+=	graphviz-[0-9]*:../../graphics/graphviz

DEPENDS+=	web2c-[0-9]*:../../print/web2c
# in case those packages are already installed by other requirement..
DEPENDS+=	texlive-collection-latex-[0-9]*:../../meta-pkgs/texlive-collection-latex
DEPENDS+=	tex-newunicodechar-[-0-9]*:../../print/tex-newunicodechar

PYTHON_VERSIONED_DEPENDENCIES=	sphinx:build

CMAKE_ARGS+=	-DENABLE_DEFAULT=False
CMAKE_ARGS+=	-DENABLE_DOXYGEN=ON
CMAKE_ARGS+=	-DENABLE_SPHINX=ON

.include "../../lang/python/versioned_dependencies.mk"
.include "../../mk/bsd.pkg.mk"
