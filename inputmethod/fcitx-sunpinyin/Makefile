# $NetBSD$

DISTNAME=	fcitx-sunpinyin-0.4.2
CATEGORIES=	inputmethod
MASTER_SITES=	http://download.fcitx-im.org/fcitx-sunpinyin/
EXTRACT_SUFX=	.tar.xz

HOMEPAGE=	http://fcitx-im.org/
COMMENT=	Sunpinyin Wrapper for Fcitx
LICENSE=	gnu-gpl-v2

USE_CMAKE=	yes
USE_LANGUAGES=	c c++
USE_TOOLS+=	msgfmt pkg-config

.include "../../inputmethod/fcitx/buildlink3.mk"
.include "../../inputmethod/sunpinyin/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
