# $FreeBSD$

PORTNAME=	rav1e
PORTVERSION=	s20190106
PORTREVISION=	1
CATEGORIES=	multimedia

MAINTAINER=	jbeich@FreeBSD.org
COMMENT=	Fast and safe AV1 encoder

LICENSE=	BSD2CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE

BUILD_DEPENDS=	${BUILD_DEPENDS_${ARCH}}
BUILD_DEPENDS_amd64=	nasm:devel/nasm

USES=		cargo
USE_GITHUB=	yes
GH_ACCOUNT=	xiph
GH_TAGNAME=	1e09055
PLIST_FILES=	bin/${PORTNAME}

CARGO_CRATES=	aho-corasick-0.6.9 \
		ansi_term-0.11.0 \
		atty-0.2.11 \
		autocfg-0.1.1 \
		backtrace-0.3.13 \
		backtrace-sys-0.1.28 \
		bindgen-0.37.4 \
		bitflags-0.4.0 \
		bitflags-1.0.4 \
		bitstream-io-0.8.2 \
		byteorder-1.2.7 \
		cast-0.2.2 \
		cc-1.0.28 \
		cexpr-0.2.3 \
		cfg-if-0.1.6 \
		chrono-0.4.6 \
		clang-sys-0.23.0 \
		clap-2.32.0 \
		cloudabi-0.0.3 \
		cmake-0.1.35 \
		criterion-0.2.5 \
		criterion-plot-0.2.7 \
		criterion-stats-0.2.5 \
		csv-1.0.5 \
		csv-core-0.1.5 \
		either-1.5.0 \
		encode_unicode-0.1.3 \
		env_logger-0.5.13 \
		failure-0.1.5 \
		failure_derive-0.1.5 \
		fuchsia-zircon-0.3.3 \
		fuchsia-zircon-sys-0.3.3 \
		glob-0.2.11 \
		handlebars-0.32.4 \
		humantime-1.2.0 \
		itertools-0.7.11 \
		itertools-num-0.1.3 \
		itoa-0.4.3 \
		kernel32-sys-0.2.2 \
		lazy_static-1.2.0 \
		libc-0.2.46 \
		libloading-0.5.0 \
		log-0.4.6 \
		memchr-1.0.2 \
		memchr-2.1.2 \
		nasm-rs-0.1.3 \
		nix-0.5.1 \
		nom-3.2.1 \
		num-integer-0.1.39 \
		num-traits-0.2.6 \
		num_cpus-1.9.0 \
		paste-0.1.4 \
		paste-impl-0.1.4 \
		peeking_take_while-0.1.2 \
		pest-1.0.6 \
		pest_derive-1.0.8 \
		pkg-config-0.3.14 \
		proc-macro-hack-0.5.4 \
		proc-macro2-0.3.5 \
		proc-macro2-0.4.24 \
		quick-error-1.2.2 \
		quote-0.3.15 \
		quote-0.5.2 \
		quote-0.6.10 \
		rand-0.4.3 \
		rand-0.5.5 \
		rand_core-0.2.2 \
		rand_core-0.3.0 \
		redox_syscall-0.1.50 \
		redox_termios-0.1.1 \
		regex-1.1.0 \
		regex-syntax-0.6.4 \
		rustc-demangle-0.1.13 \
		rustyline-1.0.0 \
		ryu-0.2.7 \
		same-file-1.0.4 \
		serde-1.0.84 \
		serde_derive-1.0.84 \
		serde_json-1.0.34 \
		simplelog-0.5.3 \
		strsim-0.7.0 \
		syn-0.11.11 \
		syn-0.15.24 \
		synom-0.11.3 \
		synstructure-0.10.1 \
		term-0.5.1 \
		termcolor-1.0.4 \
		termion-1.5.1 \
		textwrap-0.10.0 \
		thread-scoped-1.0.2 \
		thread_local-0.3.6 \
		time-0.1.41 \
		ucd-util-0.1.3 \
		unicode-width-0.1.5 \
		unicode-xid-0.0.4 \
		unicode-xid-0.1.0 \
		utf8-ranges-1.0.2 \
		vec_map-0.8.1 \
		version_check-0.1.5 \
		walkdir-2.2.7 \
		which-1.0.5 \
		winapi-0.2.8 \
		winapi-0.3.6 \
		winapi-build-0.1.1 \
		winapi-i686-pc-windows-gnu-0.4.0 \
		winapi-util-0.1.1 \
		winapi-x86_64-pc-windows-gnu-0.4.0 \
		wincolor-1.0.1 \
		y4m-0.3.1

post-install:
	@${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/${PORTNAME}

.include <bsd.port.mk>
