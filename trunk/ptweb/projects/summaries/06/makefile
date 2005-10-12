# $Id$

# .sum files that are used to create the .html files
SUM_SOURCES =  \
	ptolemyII.sum \
	actorLang.sum \
	abstractSemantics.sum \
	causalityInterfaces.sum \
	operationalSemanticsOfHS.sum \
	semanticInterpretation.sum \
	fsmExtension.sum \
	realtime.sum \
	actor-wsn.sum \
	viptos.sum \
	compositionalDataflow.sum \
	DDF_BDF.sum \
	ptIIdistributed.sum \
	wireless.sum

# other sources that are not .sum files
OTHER_SRCS =



index.html : $(SUM_SOURCES) sum2html
	-chmod a+x sum2html
	${PTII}/bin/ptjacl sum2html $(SUM_SOURCES)
	-chgrp ptolemy *.html
	-chmod g+w *.html

clean:
	rm -f index.html
