PORTNAME=	libfprint
PORTVERSION=	1.94.7
DISTVERSIONPREFIX=v
PORTREVISION=	0
CATEGORIES=	security
WWW=		https://gitlab.freedesktop.org/libfprint/libfprint/

MAINTAINER=	danfe@FreeBSD.org
COMMENT=	Library for fingerprint reader devices
WWW=		https://www.freedesktop.org/wiki/Software/fprint/

LICENSE=	LGPL21
LICENSE_FILE=	${WRKSRC}/COPYING

LIB_DEPENDS=	libnss3.so:security/nss \
		libnspr4.so:devel/nspr  \
		libudev.so:devel/libudev-devd

# The elanspi driver depends on Linux and udev
# Since we can't build it, disable it and disable udev
# We need to manually list all other drivers
MESON_ARGS= 	-Dudev_rules=disabled -Dudev_hwdb=disabled \
		-Ddrivers=virtual_image,virtual_device,virtual_device_storage,upektc_img,vfs5011,vfs7552,aes3500,aes4000,aes1610,aes1660,aes2660,aes2501,aes2550,vfs101,vfs301,vfs0050,etes603,egis0570,egismoc,vcom5s,synaptics,elan,elanmoc,uru4000,upektc,upeksonly,upekts,goodixmoc,nb1010,fpcmoc,realtek,focaltech_moc

USE_GITLAB=	yes
GL_SITE=	https://gitlab.freedesktop.org
GL_ACCOUNT=	libfprint

USES=		meson pkgconfig tar:xz
USE_LDCONFIG=	yes
INSTALL_TARGET=	install-strip

.include <bsd.port.mk>
