# $NetBSD: Makefile,v 1.4 2021/06/10 11:48:25 pin Exp $

DISTNAME=	zoxide-0.7.2
CATEGORIES=	sysutils
MASTER_SITES=	${MASTER_SITE_GITHUB:=ajeetdsouza/}
GITHUB_TAG=	v${PKGVERSION_NOREV}

MAINTAINER=	pin@NetBSD.org
HOMEPAGE=	https://github.com/ajeetdsouza/zoxide/
COMMENT=	Faster way to navigate your filesystem
LICENSE=	mit

.include "cargo-depends.mk"

USE_LANGUAGES+=		c # rust, but needs a toolchain to link

INSTALLATION_DIRS=	bin ${PKGMANDIR}/man1

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/target/release/zoxide ${DESTDIR}${PREFIX}/bin
	${INSTALL_MAN} ${WRKSRC}/man/zoxide.1 ${DESTDIR}${PREFIX}/${PKGMANDIR}/man1/zoxide.1
	${INSTALL_MAN} ${WRKSRC}/man/zoxide-add.1 ${DESTDIR}${PREFIX}/${PKGMANDIR}/man1/zoxide-add.1
	${INSTALL_MAN} ${WRKSRC}/man/zoxide-import.1 ${DESTDIR}${PREFIX}/${PKGMANDIR}/man1/zoxide-import.1
	${INSTALL_MAN} ${WRKSRC}/man/zoxide-init.1 ${DESTDIR}${PREFIX}/${PKGMANDIR}/man1/zoxide-init.1
	${INSTALL_MAN} ${WRKSRC}/man/zoxide-query.1 ${DESTDIR}${PREFIX}/${PKGMANDIR}/man1/zoxide-query.1
	${INSTALL_MAN} ${WRKSRC}/man/zoxide-remove.1 ${DESTDIR}${PREFIX}/${PKGMANDIR}/man1/zoxide-remove.1

.include "../../lang/rust/cargo.mk"
.include "../../mk/bsd.pkg.mk"
