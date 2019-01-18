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
post-extract:
	@cd ${WRKSRC} && ${SETENV} ${MAKE_ENV} ${CAT} src/version.sh src/_utils/*.sh src/commands/*.sh src/main.sh > git-secret
	@cd ${WRKSRC} && ${SETENV} ${MAKE_ENV} ${CHMOD} +x git-secret; sync

#do-install:
	#@cd ${WRKSRC} && ${SETENV} ${MAKE_ENV} ${WRKSRC}/utils/install.sh ${PREFIX}
do-install:
	@cd ${WRKSRC} && ${SETENV} ${MAKE_ENV} ${CP} git-secret ${PREFIX}/bin/git-secret
	#@cd ${WRKSRC} && ${SETENV} ${MAKE_ENV} ${CP} man/man1/*.1.gz ${PREFIX}/man/man1/
	#@cd ${WRKSRC} && ${SETENV} ${MAKE_ENV} ${CP} man/man7/*.7.gz ${PREFIX}/man/man7/

.include <bsd.port.mk>
