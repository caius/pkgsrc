# $NetBSD: Makefile,v 1.209 2017/11/23 15:59:49 wiz Exp $

DISTNAME=	pango-1.40.14
CATEGORIES=	devel fonts
MASTER_SITES=	${MASTER_SITE_GNOME:=sources/pango/${PKGVERSION_NOREV:R}/}
EXTRACT_SUFX=	.tar.xz

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://www.pango.org/
COMMENT=	Library for layout and rendering of text
LICENSE=	gnu-lgpl-v2

BUILD_DEPENDS+=		help2man-[0-9]*:../../converters/help2man

TEST_TARGET=		check
USE_LIBTOOL=		yes
USE_LANGUAGES=		c c++
USE_TOOLS+=		gmake pkg-config
GNU_CONFIGURE=		yes
CONFIGURE_ARGS+=	--sysconfdir=${PREFIX}/libdata
# Carbon has been obsoleted; force turning it off
#CONFIGURE_ENV+=		ac_cv_header_Carbon_Carbon_h=no

PKGCONFIG_OVERRIDE+=	pango.pc.in
PKGCONFIG_OVERRIDE+=	pangocairo.pc.in
PKGCONFIG_OVERRIDE+=	pangoft2.pc.in
PKGCONFIG_OVERRIDE+=	pangowin32.pc.in
PKGCONFIG_OVERRIDE+=	pangoxft.pc.in

CHECK_FILES_SKIP+=	${PREFIX}/libdata/pango/pango.modules
CHECK_PORTABILITY_SKIP+= docs/check.docs

.include "options.mk"

BUILDLINK_API_DEPENDS.glib2+=	glib2>=2.33.12
.include "../../devel/glib2/buildlink3.mk"
BUILDLINK_DEPMETHOD.gobject-introspection:= build
.include "../../devel/gobject-introspection/buildlink3.mk"
.include "../../devel/zlib/buildlink3.mk"
BUILDLINK_API_DEPENDS.fontconfig+=	fontconfig>=2.10.91
.include "../../fonts/fontconfig/buildlink3.mk"
BUILDLINK_API_DEPENDS.harfbuzz+= harfbuzz>=0.9.9
.include "../../fonts/harfbuzz/buildlink3.mk"
BUILDLINK_API_DEPENDS.cairo+=	cairo>=1.12.10
.include "../../graphics/cairo/buildlink3.mk"
.include "../../graphics/cairo-gobject/buildlink3.mk"
.include "../../graphics/freetype2/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
