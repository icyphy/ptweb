# $Id$

# .sum files that are used to create the .html files
SUM_SOURCES =  \
	ptolemyII.sum \
	copernicus03.sum \
	hyzheng03.sum \
	tinygals.sum \
	starcharts.sum \
	vergil03.sum \
	ptplot03.sum \
	ePtolemy03.sum \
	cal03.sum

# other sources that are not .sum files 
OTHER_SRCS =



index.html : $(SUM_SOURCES) sum2html
	-chmod a+x sum2html
	c:/hyzheng/ptII/bin/ptjacl sum2html $(SUM_SOURCES)
	-chgrp ptolemy *.html
	-chmod g+w *.html

clean:
	rm -f index.html
