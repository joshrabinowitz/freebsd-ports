# $FreeBSD$

PORTNAME=	minio
PORTVERSION=	${GH_TAGNAME:S/RELEASE.//:S/Z//:S/T/-/:S/-/./g}
CATEGORIES=	www

MAINTAINER=	swills@FreeBSD.org
COMMENT=	Amazon S3 compatible object storage server

LICENSE=	APACHE20

BUILD_DEPENDS=	go>=1.9.4:lang/go

USES=		compiler

USE_GITHUB=	yes
GH_TAGNAME=	RELEASE.2019-01-16T21-44-08Z
GH_SUBDIR=	src/github.com/${PORTNAME}/${PORTNAME}
COMMIT_ID=	8766c5eb22c1dc59721ad8a2c4c6fcf37bb2aad2

PLIST_FILES=	bin/minio

USE_RC_SUBR=	minio

USERS=		minio
GROUPS=		minio

SUB_LIST=	USER="${USERS}" \
		GROUP="${GROUPS}"

post-patch:
	@${CP} ${WRKSRC}/pkg/cpu/counter_linux.go ${WRKSRC}/pkg/cpu/counter_freebsd.go

do-build:
	@cd ${WRKSRC}/${GH_SUBDIR} ; \
	${SETENV} ${MAKE_ENV} GOPATH=${WRKSRC} CGO_ENABLED=0 go build \
		--ldflags '-X github.com/minio/minio/cmd.Version=${GH_TAGNAME:C/RELEASE\.//:C|(..)-(..)-(..)Z|\1:\2:\3Z|} -X github.com/minio/minio/cmd.ReleaseTag=${GH_TAGNAME} -X github.com/minio/minio/cmd.CommitID=${COMMIT_ID} -X github.com/minio/minio/cmd.GOPATH=${WRKSRC} -s -w' -o ${WRKSRC}/bin/minio

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/bin/${PORTNAME} ${STAGEDIR}${PREFIX}/bin/${PORTNAME}

.include <bsd.port.mk>
