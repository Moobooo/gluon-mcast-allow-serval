serval-mesh for android firewall rule
============

Create a file "modules" with the following content in your site directory:</a>

# Modules

GLUON_SITE_FEEDS="mcast-allow-serval"<br>
PACKAGES_mcast-allow-serval_REPO=https://github.com/Moobooo/gluon-mcast-allow-serval.git<br>
PACKAGES_mcast-allow-serval_COMMIT=fc8bee4b94a540741fd83b6fe0b9bd53f8f013c0<br>

With this done you can add the package gluon-ssid-changer to your site.mk

# site.mk

GLUON_SITE_PACKAGES := \
......
	      mcast-allow-serval \
......

DEFAULT_GLUON_RELEASE := 15.12-v2015.2-exp-AKA47-$(shell date '+%Y%m%d')

GLUON_RELEASE ?= $(DEFAULT_GLUON_RELEASE)

GLUON_PRIORITY ?= 0
GLUON_BRANCH ?= experimental
export GLUON_BRANCH

GLUON_TARGET ?= ar71xx-generic
export GLUON_TARGET

GLUON_LANGS ?= de

