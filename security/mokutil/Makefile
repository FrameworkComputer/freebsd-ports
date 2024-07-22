PORTNAME=	mokutil
PORTVERSION=	0.7.2
PORTREVISION=	0
CATEGORIES=	security

MAINTAINER=	git@danielschaefer.me
COMMENT=	Utility to manupulate UEFI Secureboot Machine Owner Keys (MOK)
WWW=		https://github.com/lcp/mokutil

LICENSE=	GPLv3+
LICENSE_FILE=   ${WRKSRC}/COPYING

# TODO: Depends on libkeyutils, which depends on Linux kernel interfaces
# Needs upstream to fix it
LIB_DEPENDS=	libefivar.so:devel/efivar

USES=		gmake libtool pkgconfig ssl autoreconf
USE_GITHUB=     yes
GH_ACCOUNT=     lcp
GNU_CONFIGURE=	yes

PLIST_FILES=	bin/mokutil \
		share/man/man1/mokutil.1.gz

.include <bsd.port.mk>
