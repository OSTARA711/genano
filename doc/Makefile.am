SUBDIRS =
BUILT_SOURCES =

dist_html_DATA = faq.html

dist_man_MANS = gen.1 rgen.1
html_pages = gen.1.html rgen.1.html

if USE_NANORC
dist_man_MANS += nanorc.5
html_pages += nanorc.5.html
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
