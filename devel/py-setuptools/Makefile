# $NetBSD: Makefile,v 1.147 2018/02/11 18:47:58 wiz Exp $

DISTNAME=	setuptools-38.5.1
PKGNAME=	${PYPKGPREFIX}-${DISTNAME}
CATEGORIES=	devel python
MASTER_SITES=	${MASTER_SITE_PYPI:=s/setuptools/}
EXTRACT_SUFX=	.zip

MAINTAINER=	joerg@NetBSD.org
HOMEPAGE=	https://pypi.python.org/pypi/setuptools
COMMENT=	New Python packaging system
LICENSE=	python-software-foundation OR zpl-2.0

DEPENDS+=		${PYPKGPREFIX}-expat-[0-9]*:../../textproc/py-expat
# included again since 36.0 in vendored version
#DEPENDS+=		${PYPKGPREFIX}-appdirs-[0-9]*:../../devel/py-appdirs
#DEPENDS+=		${PYPKGPREFIX}-packaging-[0-9]*:../../devel/py-packaging
#DEPENDS+=		${PYPKGPREFIX}-six-[0-9]*:../../lang/py-six
# needed for tests, but would introduce dependency cycle
#BUILD_DEPENDS+=	${PYPKGPREFIX}-test-runner-[0-9]*:../../devel/py-test-runner

REPLACE_PYTHON+=	setuptools/command/easy_install.py

PYSETUPTESTTARGET=	pytest

.include "../../lang/python/application.mk"
.include "../../lang/python/distutils.mk"
.include "../../mk/bsd.pkg.mk"
