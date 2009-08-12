man_MANS = memcached.1

EXTRA_DIST = *.txt

BUILT_SOURCES=

if BUILD_SPECIFICATIONS
BUILT_SOURCES += protocol-binary.txt protocol-binary-range.txt
MOSTLYCLEANFILES = protocol-binary.txt protocol-binary-range.txt
endif

.full.txt:
	${XML2RFC} $< $@

.xml.chk: xml2rfc/rfc2629-refchk.xsl
	${XSLTPROC} xml2rfc/rfc2629-refchk.xsl $< >$@

.xml.full: xml2rfc/rfc2629-noinc.xsl
	${XSLTPROC) xml2rfc/rfc2629-noinc.xsl $< >$@

