PORTNAME=	sbctl
PORTVERSION=	0.14
PORTREVISION=	0
CATEGORIES=	security

MAINTAINER=	git@danielschaefer.me
COMMENT=	Secure Boot key manager
WWW=		https://github.com/foxboron/sbctl

LICENSE=	MIT
LICENSE_FILE=   ${WRKSRC}/LICENSE

USE_GITHUB=     yes
GH_TUPLE=	foxboron:sbctl:${PORTVERSION}

USES=           go tar:xz

GO_PKGNAME=	github.com/Foxboron/sbctl

PLIST_FILES=	bin/sbctl

.include <bsd.port.mk>
