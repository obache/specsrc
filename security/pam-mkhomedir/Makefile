# $NetBSD: Makefile,v 1.10 2020/10/23 09:20:59 tnn Exp $

DISTNAME=	pam-mkhomedir-1
PKGREVISION=	1
CATEGORIES=	security
MASTER_SITES=	# empty
DISTFILES=	# empty

MAINTAINER=	pkgsrc-users@NetBSD.org
COMMENT=	Pluggable authentication module for automatic homedir creation

INSTALLATION_DIRS=	lib/security
LDLIBS=			-lpam

USE_LIBTOOL=		yes

WRKSRC=			${WRKDIR}

do-extract:
	${CP} ${FILESDIR}/pam_mkhomedir.c ${WRKSRC}

do-build:
	cd ${WRKSRC} && ${SHLIBTOOL} --mode=compile ${CC} ${CFLAGS}	\
		-c pam_mkhomedir.c
	cd ${WRKSRC} && ${SHLIBTOOL} --mode=link ${CC} ${LDFLAGS}	\
		-avoid-version -module ${LDLIBS} -o pam_mkhomedir.la	\
		-rpath ${PREFIX}/lib/security pam_mkhomedir.lo

do-install:
	${SHLIBTOOL} --mode=install ${INSTALL_PROGRAM} -c		\
		${WRKSRC}/pam_mkhomedir.la ${DESTDIR}${PREFIX}/lib/security

.include "../../mk/pam.buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
