# $Id$

# .sum files that are used to create the .html files
SUM_SOURCES = ptolemyII.sum \
	  cont_and_disc.sum \
	  copernicus02.sum \
	  e_Ptolemy.sum \
	  ndest.sum \
	  starcharts.sum \
	  vergil02.sum \
	  vogel02.sum \
	  winthrop02.sum \
	  yuhong02.sum

# other sources that are not .sum files 
OTHER_SRCS = \
	  winthrop02.jpg 


index.html : $(SUM_SOURCES) sum2html
	-chmod a+x sum2html
	sum2html $(SUM_SOURCES)
	-chgrp ptolemy *.html
	-chmod g+w *.html

clean:
	rm -f index.html
