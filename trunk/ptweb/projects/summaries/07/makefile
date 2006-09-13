# $Id$

# .sum files that are used to create the .html files
SUM_SOURCES =  \
	ptolemyII.sum \
	DDF_BDF.sum \
	abstractSemantics.sum \
	actor-wsn.sum \
	actorLang.sum \
	causalityInterfaces.sum \
	compositionalDataflow.sum \
	operationalSemanticsOfHS.sum \
	ptides.sum \
	ptIIdistributed.sum \
	realtime.sum \
	semanticInterpretation.sum \
	viptos.sum 


# other sources that are not .sum files
OTHER_SRCS =



index.html : $(SUM_SOURCES) sum2html
	-chmod a+x sum2html
	${PTII}/bin/ptjacl sum2html $(SUM_SOURCES)
	-chgrp ptolemy *.html
	-chmod g+w *.html

clean:
	rm -f index.html
