# $Id$

SOURCES = ptolemyII.sum \
	  cont_and_disc.sum \
	  copernicus02.sum \
	  e_Ptolemy.sum \
	  ndest.sum \
	  starcharts.sum \
	  vergil02.sum \
	  vogel02.sum \
	  winthrop02.sum \
	  winthrop02.jpg \
	  yuhong02.sum


index.html : $(SOURCES) sum2html
	-chmod a+x sum2html
	sum2html $(SOURCES)
	-chgrp ptolemy *.html
	-chmod g+w *.html

clean:
	rm -f index.html
