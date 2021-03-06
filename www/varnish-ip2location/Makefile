# Created by: Ryan Steinmetz <zi@FreeBSD.org>
# $FreeBSD$

PORTNAME=	ip2location
PORTVERSION=	1.0.1
CATEGORIES=	www
PKGNAMEPREFIX=	varnish-

MAINTAINER=	zi@FreeBSD.org
COMMENT=	Varnish Module (vmod) for ip2location

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE.TXT

LIB_DEPENDS=	libIP2Location.so:net/ip2location
BUILD_DEPENDS=	rst2man:textproc/py-docutils@${PY_FLAVOR}

USES=		autoreconf:build libtool pkgconfig python:build varnish:6
USE_LDCONFIG=	yes

PLIST_FILES=	lib/varnish/vmods/libvmod_ip2location.so

GNU_CONFIGURE=	yes
CONFIGURE_ARGS=	--disable-static
INSTALL_TARGET=	install-strip
DOCSDIR=	${PREFIX}/share/doc/vmod-dynamic
MAKE_JOBS_UNSAFE=	yes

CFLAGS+=	-I${WRKSRC}/src

USE_GITHUB=	yes
GH_ACCOUNT=	ip2location
GH_PROJECT=	${PORTNAME}-varnish
GH_TAGNAME=	25928cf

OPTIONS_DEFINE=	DOCS

post-extract:
	@(cd ${WRKDIR} && ${LN} -sf IP2Location-Varnish-${GH_TAGNAME} \
		${PORTNAME}-${PKGNAMEPREFIX}${GH_TAGNAME})

post-patch:
	${REINPLACE_CMD} 's|$${VARNISHAPI_DATAROOTDIR}|${LOCALBASE}/share|' \
		${WRKSRC}/Makefile.am

pre-configure:
	(cd ${WRKSRC} && ${SH} ./autogen.sh)

.include <bsd.port.mk>
