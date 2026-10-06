# Path: ~/gen/doc/Makefile.am

SUBDIRS =
BUILT_SOURCES =

dist_html_DATA = faq.html

dist_man_MANS = gen.1 rgen.1

if USE_NANORC
BUILT_SOURCES += nanorc
dist_man_MANS += nanorc.5
sysconf_DATA = nanorc
html_pages = nanorc.5.html
endif

gen.1.html: gen.1
	groff -t -mandoc -Thtml < $? > $@
nanorc.5.html: nanorc.5
	groff -t -mandoc -Thtml < $? > $@
rgen.1.html: rgen.1
	groff -t -mandoc -Thtml < $? > $@

if GROFF_HTML
BUILT_SOURCES += $(html_pages)
dist_html_DATA += $(html_pages)
endif

info_TEXINFOS = nano.texi

BUILT_SOURCES += nano.html
dist_html_DATA += nano.html

AM_MAKEINFOHTMLFLAGS = --no-split -c HEADERS=0

EXTRA_DIST = $(BUILT_SOURCES) $(info_TEXINFOS)
