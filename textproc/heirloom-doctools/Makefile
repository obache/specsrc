# $NetBSD: Makefile,v 1.5 2020/01/18 23:35:26 rillig Exp $

DISTNAME=	heirloom-doctools-160308
CATEGORIES=	textproc
MASTER_SITES=	${MASTER_SITE_GITHUB:=n-t-roff/}

MAINTAINER=	carsten.kunze@arcor.de
HOMEPAGE=	https://n-t-roff.github.io/heirloom/doctools.html
COMMENT=	Modernized troff implementation
LICENSE=	cddl-1.0

MAKE_JOBS_SAFE=	no

USE_LANGUAGES=	c c++
USE_TOOLS+=	lex yacc

MAKE_FLAGS=	CC=${CC:Q} \
		CCC=${CXX:Q} \
		CFLAGS=${CFLAGS:Q} \
		RANLIB=ranlib \
		INSTALL=install \
		ROOT=${DESTDIR} \
		BINDIR=${PREFIX}/heirloom-doctools/bin \
		MANDIR=${PREFIX}/heirloom-doctools/man \
		LIBDIR=${PREFIX}/libexec/heirloom-doctools \
		MACDIR=${PREFIX}/share/heirloom-doctools/tmac \
		FNTDIR=${PREFIX}/share/heirloom-doctools/font \
		TABDIR=${PREFIX}/share/heirloom-doctools/nterm \
		HYPDIR=${PREFIX}/share/heirloom-doctools/hyphen \
		PUBDIR=${PREFIX}/share/heirloom-doctools/pub \
		PSTDIR=${PREFIX}/share/heirloom-doctools/font/devpost/postscript \
		REFDIR=${PREFIX}/libexec/heirloom-doctools/reftools

MAKE_FILE=	makefile
BUILD_TARGET=	dummy

.include "../../mk/bsd.pkg.mk"
