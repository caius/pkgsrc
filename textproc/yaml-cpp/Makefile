# $NetBSD: Makefile,v 1.6 2018/02/04 17:05:15 fhajny Exp $

DISTNAME=	yaml-cpp-0.6.1
CATEGORIES=	textproc
MASTER_SITES=	${MASTER_SITE_GITHUB:=jbeder/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://github.com/jbeder/yaml-cpp/
COMMENT=	YAML parser and emitter for C++
LICENSE=	mit

GITHUB_TAG=	${DISTNAME}
EXTRACT_USING=	bsdtar

USE_CMAKE=		yes
USE_LANGUAGES=		c c++11
CMAKE_ARGS+=		-DBUILD_SHARED_LIBS=ON
CMAKE_ARGS+=		-DYAML_CPP_BUILD_TESTS=OFF # issue 539
PKGCONFIG_OVERRIDE+=	yaml-cpp.pc.cmake

TEST_ENV+=	LD_LIBRARY_PATH=${WRKSRC}
TEST_TARGET=	test

.include "../../mk/bsd.pkg.mk"
