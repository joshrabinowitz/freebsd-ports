# $FreeBSD$

PORTNAME=	git-secret
DISTVERSION=	0.2.5
CATEGORIES=	security

MAINTAINER=	mail@sobolevn.me
COMMENT=	Bash tool to store your private data inside a git repository

LICENSE=	MIT
#MASTER_SITES=	https://github.com/sobolevn/git-secret/archive/

#BUILD_DEPENDS=	bash:shells/bash gpg2:security/gnupg gawk:lang/gawk

USE_GITHUB=	yes
GH_ACCOUNT=	sobolevn
GH_PROJECT=	git-secret
GH_TAGNAME=	94d5ae4

SCRIPTS=	git-secret
ALL_TARGET=	git-secret

#post-extract:
#	@cd ${WRKSRC} && ${SETENV} ${MAKE_ENV} make test

do-install:
	@cd ${WRKSRC} && ${SETENV} ${MAKE_ENV} ${WRKSRC}/utils/install.sh ${PREFIX}

.include <bsd.port.mk>
