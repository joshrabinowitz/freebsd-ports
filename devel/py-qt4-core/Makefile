# Created by: Danny Pansters <danny@ricin.com>
# $FreeBSD$

PORTNAME=	core
PORTREVISION=	8
PORTEPOCH=	1
CATEGORIES=	devel python

MAINTAINER=	kde@FreeBSD.org
COMMENT=	Python bindings for the Qt4 toolkit, QtCore module

DEPRECATED=		Qt4 has been EOL since december 2015
EXPIRATION_DATE=	2019-03-15

CONFIGURE_ARGS=		--enable QtCore
PYQT_DIST=		yes

USES=			python pyqt:4 qt:4
USE_PYTHON=		concurrent flavors py3kplist
USE_PYQT=		sip
USE_QT=			corelib qmake_build moc_build

OPTIONS_DEFINE=	API DEBUG
OPTIONS_DEFAULT=API
OPTIONS_SUB=	yes

API_DESC=		Install QtCore API for QScintilla2
API_CONFIGURE_ON=	--qsci-api --qsci-api-destdir=${PYQT_APIDIR}
API_CONFIGURE_OFF=	--no-qsci-api
API_LIB_DEPENDS=	libqscintilla2_qt4.so:devel/qscintilla2
DEBUG_CONFIGURE_ON=	--debug --trace

.include <bsd.port.pre.mk>

# Bug 180467: We need to remove the port_v${VERSION} directory that does not
# correspond to the Python version being used to avoid failures in the
# bytecompilation calls in post-install.
PLIST_SUB+=	PYTHON_MAJOR_VER="${PYTHON_MAJOR_VER}"
post-patch:
.if ${PYTHON_MAJOR_VER} == "2"
	${RM} -r ${WRKSRC}/pyuic/uic/port_v3
.elif ${PYTHON_MAJOR_VER} == "3"
	${RM} -r ${WRKSRC}/pyuic/uic/port_v2
.endif

post-install:
	${INSTALL_DATA} ${FILESDIR}/Qt.py ${STAGEDIR}${PYTHONPREFIX_SITELIBDIR}/PyQt4
	${PYTHON_CMD} ${PYTHON_LIBDIR}/compileall.py \
		-f -d ${PYTHONPREFIX_SITELIBDIR}/PyQt4 \
		${STAGEDIR}${PYTHONPREFIX_SITELIBDIR}/PyQt4
	${PYTHON_CMD} -O ${PYTHON_LIBDIR}/compileall.py \
		-f -d ${PYTHONPREFIX_SITELIBDIR}/PyQt4 \
		${STAGEDIR}${PYTHONPREFIX_SITELIBDIR}/PyQt4

.include <bsd.port.post.mk>
