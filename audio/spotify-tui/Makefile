# $FreeBSD$

PORTNAME=	spotify-tui
DISTVERSIONPREFIX=	v
DISTVERSION=	0.21.0
PORTREVISION=	1
CATEGORIES=	audio

MAINTAINER=	vulcan@wired.sh
COMMENT=	Spotify for the terminal written in Rust

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

USES=		cargo localbase:ldflags python:3.6+,build ssl xorg
USE_GITHUB=	yes
GH_ACCOUNT=	Rigellute
USE_XORG=	xcb

CARGO_CRATES=	addr2line-0.12.0 \
		adler32-1.1.0 \
		aho-corasick-0.7.10 \
		ansi_term-0.11.0 \
		anyhow-1.0.31 \
		arc-swap-0.4.6 \
		arrayref-0.3.6 \
		arrayvec-0.5.1 \
		atty-0.2.14 \
		autocfg-0.1.7 \
		autocfg-1.0.0 \
		backtrace-0.3.49 \
		base64-0.10.1 \
		base64-0.11.0 \
		bitflags-1.2.1 \
		blake2b_simd-0.5.10 \
		block-0.1.6 \
		bumpalo-3.2.1 \
		byteorder-1.3.4 \
		bytes-0.4.12 \
		bytes-0.5.4 \
		cassowary-0.3.0 \
		cc-1.0.52 \
		cfg-if-0.1.10 \
		chrono-0.4.11 \
		clap-2.33.1 \
		clipboard-0.5.0 \
		clipboard-win-2.2.0 \
		cloudabi-0.0.3 \
		constant_time_eq-0.1.5 \
		core-foundation-0.7.0 \
		core-foundation-sys-0.7.0 \
		crossbeam-utils-0.7.2 \
		crossterm-0.17.5 \
		crossterm_winapi-0.6.1 \
		darling-0.9.0 \
		darling_core-0.9.0 \
		darling_macro-0.9.0 \
		derive_builder-0.7.2 \
		derive_builder_core-0.5.0 \
		dirs-2.0.2 \
		dirs-sys-0.3.4 \
		dotenv-0.13.0 \
		dtoa-0.4.5 \
		either-1.5.3 \
		encoding_rs-0.8.22 \
		env_logger-0.6.2 \
		failure-0.1.8 \
		failure_derive-0.1.8 \
		fnv-1.0.6 \
		foreign-types-0.3.2 \
		foreign-types-shared-0.1.1 \
		fuchsia-cprng-0.1.1 \
		fuchsia-zircon-0.3.3 \
		fuchsia-zircon-sys-0.3.3 \
		futures-0.3.5 \
		futures-channel-0.3.5 \
		futures-core-0.3.5 \
		futures-executor-0.3.5 \
		futures-io-0.3.5 \
		futures-macro-0.3.5 \
		futures-sink-0.3.5 \
		futures-task-0.3.5 \
		futures-util-0.3.5 \
		getrandom-0.1.14 \
		gimli-0.21.0 \
		h2-0.2.5 \
		hermit-abi-0.1.12 \
		http-0.2.1 \
		http-body-0.3.1 \
		httparse-1.3.4 \
		humantime-1.3.0 \
		hyper-0.13.5 \
		hyper-tls-0.4.1 \
		ident_case-1.0.1 \
		idna-0.1.5 \
		idna-0.2.0 \
		indexmap-1.3.2 \
		iovec-0.1.4 \
		itertools-0.8.2 \
		itertools-0.9.0 \
		itoa-0.4.5 \
		js-sys-0.3.39 \
		kernel32-sys-0.2.2 \
		lazy_static-1.4.0 \
		libc-0.2.69 \
		linked-hash-map-0.5.3 \
		lock_api-0.3.4 \
		log-0.4.8 \
		malloc_buf-0.0.6 \
		matches-0.1.8 \
		memchr-2.3.3 \
		mime-0.3.16 \
		mime_guess-2.0.3 \
		miniz_oxide-0.3.7 \
		mio-0.6.22 \
		mio-named-pipes-0.1.6 \
		mio-uds-0.6.8 \
		miow-0.2.1 \
		miow-0.3.3 \
		native-tls-0.2.4 \
		net2-0.2.34 \
		num-integer-0.1.42 \
		num-traits-0.2.11 \
		num_cpus-1.13.0 \
		objc-0.2.7 \
		objc-foundation-0.1.1 \
		objc_id-0.1.1 \
		object-0.20.0 \
		once_cell-1.3.1 \
		openssl-0.10.29 \
		openssl-probe-0.1.2 \
		openssl-sys-0.9.56 \
		parking_lot-0.10.2 \
		parking_lot_core-0.7.2 \
		percent-encoding-1.0.1 \
		percent-encoding-2.1.0 \
		pin-project-0.4.16 \
		pin-project-internal-0.4.16 \
		pin-project-lite-0.1.5 \
		pin-utils-0.1.0 \
		pkg-config-0.3.17 \
		ppv-lite86-0.2.6 \
		proc-macro-hack-0.5.15 \
		proc-macro-nested-0.1.4 \
		proc-macro2-0.4.30 \
		proc-macro2-1.0.18 \
		quick-error-1.2.3 \
		quote-0.6.13 \
		quote-1.0.4 \
		rand-0.6.5 \
		rand-0.7.3 \
		rand_chacha-0.1.1 \
		rand_chacha-0.2.2 \
		rand_core-0.3.1 \
		rand_core-0.4.2 \
		rand_core-0.5.1 \
		rand_hc-0.1.0 \
		rand_hc-0.2.0 \
		rand_isaac-0.1.1 \
		rand_jitter-0.1.4 \
		rand_os-0.1.3 \
		rand_pcg-0.1.2 \
		rand_xorshift-0.1.1 \
		random-0.12.2 \
		rdrand-0.4.0 \
		redox_syscall-0.1.56 \
		redox_users-0.3.4 \
		regex-1.3.7 \
		regex-syntax-0.6.17 \
		remove_dir_all-0.5.2 \
		reqwest-0.10.4 \
		rspotify-0.9.0 \
		rust-argon2-0.7.0 \
		rustc-demangle-0.1.16 \
		rustc-serialize-0.3.24 \
		ryu-1.0.4 \
		schannel-0.1.19 \
		scopeguard-1.1.0 \
		security-framework-0.4.4 \
		security-framework-sys-0.4.3 \
		serde-1.0.114 \
		serde_derive-1.0.114 \
		serde_json-1.0.56 \
		serde_urlencoded-0.6.1 \
		serde_yaml-0.8.13 \
		signal-hook-0.1.15 \
		signal-hook-registry-1.2.0 \
		slab-0.4.2 \
		smallvec-1.4.0 \
		socket2-0.3.12 \
		strsim-0.7.0 \
		strsim-0.8.0 \
		syn-0.15.44 \
		syn-1.0.33 \
		synstructure-0.12.3 \
		tempfile-3.1.0 \
		termcolor-1.1.0 \
		textwrap-0.11.0 \
		thiserror-1.0.16 \
		thiserror-impl-1.0.16 \
		thread_local-1.0.1 \
		time-0.1.43 \
		tokio-0.2.22 \
		tokio-macros-0.2.5 \
		tokio-socks-0.2.2 \
		tokio-tls-0.3.1 \
		tokio-util-0.3.1 \
		tower-service-0.3.0 \
		try-lock-0.2.2 \
		tui-0.9.5 \
		unicase-2.6.0 \
		unicode-bidi-0.3.4 \
		unicode-normalization-0.1.12 \
		unicode-segmentation-1.6.0 \
		unicode-width-0.1.8 \
		unicode-xid-0.1.0 \
		unicode-xid-0.2.0 \
		url-1.7.2 \
		url-2.1.1 \
		vcpkg-0.2.8 \
		vec_map-0.8.2 \
		version_check-0.9.1 \
		want-0.3.0 \
		wasi-0.9.0+wasi-snapshot-preview1 \
		wasm-bindgen-0.2.62 \
		wasm-bindgen-backend-0.2.62 \
		wasm-bindgen-futures-0.4.12 \
		wasm-bindgen-macro-0.2.62 \
		wasm-bindgen-macro-support-0.2.62 \
		wasm-bindgen-shared-0.2.62 \
		web-sys-0.3.39 \
		webbrowser-0.5.2 \
		widestring-0.4.0 \
		winapi-0.2.8 \
		winapi-0.3.8 \
		winapi-build-0.1.1 \
		winapi-i686-pc-windows-gnu-0.4.0 \
		winapi-util-0.1.5 \
		winapi-x86_64-pc-windows-gnu-0.4.0 \
		winreg-0.6.2 \
		ws2_32-sys-0.2.1 \
		x11-clipboard-0.3.3 \
		xcb-0.8.2 \
		yaml-rust-0.4.3

BINARY_ALIAS=	python3=${PYTHON_CMD}

SUB_FILES=	pkg-message
PLIST_FILES=	bin/spt
PORTDOCS=	CHANGELOG.md README.md

OPTIONS_DEFINE=	DOCS SPOTIFYD
SPOTIFYD_DESC=	Lightweight Spotify client daemon

SPOTIFYD_RUN_DEPENDS=	spotifyd:audio/spotifyd

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/spt

post-install-DOCS-on:
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	${INSTALL_DATA} ${PORTDOCS:S|^|${WRKSRC}/|} ${STAGEDIR}${DOCSDIR}

.include <bsd.port.mk>
