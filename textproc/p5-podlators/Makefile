# $NetBSD: Makefile,v 1.22 2017/12/30 15:03:43 wiz Exp $

DISTNAME=	podlators-4.10
PKGNAME=	p5-${DISTNAME}
CATEGORIES=	devel perl5
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=Pod/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://search.cpan.org/dist/podlators/
COMMENT=	Collection of pod related perl modules
LICENSE=	${PERL5_LICENSE}

#DEPENDS+=	{perl>=5.10.1,p5-Pod-Simple>=3.06}:../../textproc/p5-Pod-Simple

PERL5_PACKLIST=		auto/Pod/.packlist

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
