# Created by: KIMURA Yasuhiro <yasu@utahime.org>
# $FreeBSD$

PORTNAME=	yaml-mode.el
PORTVERSION=	0.0.13
PORTREVISION=	2
DISTVERSIONPREFIX=	v
CATEGORIES=	textproc elisp
PKGNAMESUFFIX=	-${EMACS_PORT_NAME}

MAINTAINER=	yasu@utahime.org
COMMENT=	Simple major mode to edit YAML file for Emacsen

LICENSE=	GPLv2+
LICENSE_FILE=	${WRKSRC}/LICENSE.txt

USE_GITHUB=	yes
GH_ACCOUNT=	yoshiki
GH_PROJECT=	yaml-mode

USE_EMACS=	yes

MAKE_ENV=	LISPDIR=${LISPDIR}

LISPDIR=	${STAGEDIR}${PREFIX}/${EMACS_VERSION_SITE_LISPDIR}

OPTIONS_DEFINE=	DOCS

pre-install:
	@${MKDIR} ${LISPDIR}

post-install-DOCS-on:
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
.for file in Changes README
	${INSTALL_MAN} ${WRKSRC}/${file} ${STAGEDIR}${DOCSDIR}
.endfor

.include <bsd.port.mk>
