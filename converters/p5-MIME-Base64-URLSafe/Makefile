# $NetBSD: Makefile,v 1.17 2021/05/24 19:49:22 wiz Exp $

DISTNAME=	MIME-Base64-URLSafe-0.01
PKGNAME=	p5-${DISTNAME}
PKGREVISION=	13
CATEGORIES=	converters perl5
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=MIME/}

MAINTAINER=	abs@NetBSD.org
HOMEPAGE=	https://metacpan.org/release/MIME-Base64-URLSafe
COMMENT=	Perl version of Python's URL-safe base64 codec

PERL5_PACKLIST=		auto/MIME/Base64/URLSafe/.packlist

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
