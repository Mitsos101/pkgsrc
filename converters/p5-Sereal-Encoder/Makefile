# $NetBSD: Makefile,v 1.21 2020/06/18 19:55:28 fcambus Exp $

DISTNAME=	Sereal-Encoder-4.014
PKGNAME=	p5-${DISTNAME}
CATEGORIES=	security perl5 converters
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=../../CPAN/authors/id/Y/YV/YVES/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://metacpan.org/release/Sereal-Encoder
COMMENT=	Perl5 module for fast, compact, powerful binary serialization
LICENSE=	${PERL5_LICENSE}

BUILD_DEPENDS+=	p5-Test-Deep-[0-9]*:../../devel/p5-Test-Deep
BUILD_DEPENDS+=	p5-Test-LongString-[0-9]*:../../devel/p5-Test-LongString
BUILD_DEPENDS+=	p5-Test-Warn-[0-9]*:../../devel/p5-Test-Warn
BUILD_DEPENDS+=	p5-Sereal-Decoder>=4.002:../../converters/p5-Sereal-Decoder

PERL5_PACKLIST=		auto/Sereal/Encoder/.packlist

# dependency problem in 4.002 with zstd/
MAKE_JOBS_SAFE=		no

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
