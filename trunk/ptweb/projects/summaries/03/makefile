# $Id$

# .sum files that are used to create the .html files
SUM_SOURCES =  \
	copernicus03.sum \
	e_Ptolemy.sum \
	hyzheng03.sum \
	ndest.sum \
	ptolemyII.sum \
	starcharts.sum \
	vergil03.sum 

# other sources that are not .sum files 
OTHER_SRCS =



index.html : $(SUM_SOURCES) sum2html
	-chmod a+x sum2html
	sum2html $(SUM_SOURCES)
	-chgrp ptolemy *.html
	-chmod g+w *.html

clean:
	rm -f index.html
