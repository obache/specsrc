# $NetBSD: Makefile,v 1.3 2018/12/09 21:05:36 adam Exp $

DISTNAME=	mod_authnz_external-${DISTVERS}
PKGNAME=	${APACHE_PKG_PREFIX}-authnz-external-${DISTVERS}
CATEGORIES=	www
MASTER_SITES=	https://github.com/phokz/mod-auth-external/archive/

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://github.com/phokz/mod-auth-external/tree/master/mod_authnz_external
COMMENT=	Apache module for external program authentication
LICENSE=	apache-1.1

PKG_APACHE_ACCEPTED=	apache24

WRKSRC=		${WRKDIR}/mod-auth-external-${DISTNAME}
APACHE_MODULE_NAME=	mod_authnz_external.${MODULE_EXT}

DISTVERS=	3.3.1
MODULE_EXT=	la
MESSAGE_SUBST+=	MODULE_NAME=authnz_external_module

INSTALLATION_DIRS+=	share/doc/authnz-external

post-install:
	${INSTALL_DATA} ${WRKSRC}/AUTHENTICATORS \
		${DESTDIR}${PREFIX}/share/doc/authnz-external
	${INSTALL_DATA} ${WRKSRC}/INSTALL \
		${DESTDIR}${PREFIX}/share/doc/authnz-external
	${INSTALL_DATA} ${WRKSRC}/INSTALL.HARDCODE \
		${DESTDIR}${PREFIX}/share/doc/authnz-external
	${INSTALL_DATA} ${WRKSRC}/TODO \
		${DESTDIR}${PREFIX}/share/doc/authnz-external
	${INSTALL_DATA} ${WRKSRC}/UPGRADE \
		${DESTDIR}${PREFIX}/share/doc/authnz-external

.include "../../mk/apache.module.mk"
.include "../../mk/bsd.pkg.mk"
