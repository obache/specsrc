# $NetBSD: Makefile,v 1.8 2021/06/02 10:25:32 adam Exp $

DISTNAME=	faudio-21.06
CATEGORIES=	audio
MASTER_SITES=	${MASTER_SITE_GITHUB:=FNA-XNA/}
GITHUB_PROJECT=	FAudio

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://fna-xna.github.io/
COMMENT=	Accuracy-focused XAudio reimplementation for open platforms
LICENSE=	zlib

WRKSRC=		${WRKDIR}/${GITHUB_PROJECT}-${PKGVERSION_NOREV}
USE_CMAKE=	yes
USE_TOOLS+=	pkg-config
USE_LANGUAGES=	c c++

CMAKE_ARGS+=	-DFFMPEG=ON

.include "../../devel/SDL2/buildlink3.mk"
.include "../../multimedia/ffmpeg4/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
