# $Id$

# .sum files that are used to create the .html files
SUM_SOURCES =  \
	ptolemyII.sum \
	copernicus04.sum \
	sdfStudy04.sum \
	tinygals.sum \
	vergil04.sum \
	ptplot04.sum \
	ePtolemy04.sum \
	cal04.sum \
	softwalls.sum \
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
