# $Id$

# .sum files that are used to create the .html files
SUM_SOURCES =  \
	ptolemyII.sum \
	copernicus05.sum \
	distributedComponentManagement.sum \
	compositionalityAnalysis.sum \
        softDevel05.sum \
	tinygals.sum \
	vergil05.sum \
	ptplot05.sum \
	softwalls.sum \
        sensorNetworks.sum \
	wireless.sum \
	cacheAwareScheduling.sum \
	structuredIA.sum \
	smachine.sum \
        DDF_BDF.sum \
	simTimedMoCs.sum

# other sources that are not .sum files 
OTHER_SRCS =



index.html : $(SUM_SOURCES) sum2html
	-chmod a+x sum2html
	${PTII}/bin/ptjacl sum2html $(SUM_SOURCES)
	-chgrp ptolemy *.html
	-chmod g+w *.html

clean:
	rm -f index.html
