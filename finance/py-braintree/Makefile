# $NetBSD: Makefile,v 1.6 2018/02/12 08:34:00 adam Exp $

DISTNAME=	braintree-3.41.0
PKGNAME=	${PYPKGPREFIX}-${DISTNAME}
CATEGORIES=	finance python
MASTER_SITES=	${MASTER_SITE_PYPI:=b/braintree/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://developers.braintreepayments.com/python/sdk/server/overview
COMMENT=	Braintree Python Library
LICENSE=	mit

DEPENDS+=	${PYPKGPREFIX}-requests>=0.11.1:../../devel/py-requests

USE_LANGUAGES=	# none

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
