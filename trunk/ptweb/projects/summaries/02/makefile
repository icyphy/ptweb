# $Id$

SOURCES = ptolemyII.sum \
	  cont_and_disc.sum \
	  e_Ptolemy.sum \
	  nest.sum \
	  starcharts.sum \
	  vergil02.sum \
	  vogel02.sum \
	  vthreads.sum \
	  winthrop02.sum \
	  yuhong02.sum


index.html : $(SOURCES) sum2html
	-chmod a+x sum2html
	sum2html $(SOURCES)
	-chgrp ptolemy *.html
	-chmod g+w *.html

clean:
	rm -f index.html
