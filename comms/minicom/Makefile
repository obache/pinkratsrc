# $NetBSD: Makefile,v 1.70 2018/07/04 13:40:12 jperkin Exp $

DISTNAME=	minicom-2.7.1
CATEGORIES=	comms
MASTER_SITES=	https://alioth.debian.org/frs/download.php/file/4215/

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://alioth.debian.org/projects/minicom/
COMMENT=	MS-DOS Telix serial communication program "workalike"
LICENSE=	gnu-gpl-v2

DEPENDS+=	gkermit-[0-9]*:../../comms/gkermit
DEPENDS+=	lrzsz-[0-9]*:../../comms/lrzsz

INSTALLATION_DIRS=	share/examples/minicom

USE_PKGLOCALEDIR=	yes
USE_TOOLS+=		gmake msgfmt
GNU_CONFIGURE=		yes
CONFIGURE_ARGS+=	--sysconfdir=${PKG_SYSCONFDIR}

PKG_SYSCONFSUBDIR=	minicom
EGDIR=			${PREFIX}/share/examples/minicom

SUBST_CLASSES+=		minicom
SUBST_MESSAGE.minicom=	Fixing hardcoded paths.
SUBST_STAGE.minicom=	pre-configure
SUBST_FILES.minicom=	src/rwconf.c
SUBST_VARS.minicom=	PREFIX

.include "options.mk"

.include "../../converters/libiconv/buildlink3.mk"
.include "../../devel/gettext-lib/buildlink3.mk"
.include "../../mk/termcap.buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
