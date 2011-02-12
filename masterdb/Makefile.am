
master_PRE = masterdb.xml
sgmldbs_DATA =				\
	$(master_PRE:xml=html.xml)	\
	$(master_PRE:xml=pdf.xml)	\
	$(master_PRE:xml=ps.xml)	\
	$(master_PRE:xml=txt.xml)

EXTRA_DIST = $(master_PRE)
CLEANFILES = $(sgmldbs_DATA)

DIR_SUBSTS = 					\
	-e 's|@sgmldbsdir[@]|$(sgmldbsdir)|g' 	\
	-e 's|@datarootdir[@]|$(datarootdir)|g'

%.html.xml: %.xml
	$(AM_V_GEN)$(SED) $(DIR_SUBSTS) -e 's|__ext__|html|g' < $< > $@

%.pdf.xml: %.xml
	$(AM_V_GEN)$(SED) $(DIR_SUBSTS) -e 's|__ext__|pdf|g' < $< > $@

%.ps.xml: %.xml
	$(AM_V_GEN)$(SED) $(DIR_SUBSTS) -e 's|__ext__|ps|g' < $< > $@

%.txt.xml: %.xml
	$(AM_V_GEN)$(SED) $(DIR_SUBSTS) -e 's|__ext__|txt|g' < $< > $@
