# $NetBSD: Makefile,v 1.5 2017/09/16 19:27:07 wiz Exp $

DISTNAME=	py-bcrypt-0.4
PKGNAME=	${PYPKGPREFIX}-${DISTNAME}
CATEGORIES=	python security
MASTER_SITES=	${MASTER_SITE_PYPI:=p/py-bcrypt/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://pypi.python.org/pypi/bcrypt/
COMMENT=	Provides bcrypt password hashing and key derivation in python
LICENSE=	isc AND modified-bsd AND original-bsd

CONFLICTS+=	${PYPKGPREFIX}-bcrypt-[0-9]*:../../security/py-bcrypt

CFLAGS.SunOS+=	-Du_int8_t=uint8_t -Du_int16_t=uint16_t
CFLAGS.SunOS+=	-Du_int32_t=uint32_t -Du_int64_t=uint64_t

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
