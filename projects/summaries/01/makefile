# $Id$

SOURCES = ptolemyII.sum \
	  chf.sum \
	  cont_and_disc.sum \
	  e_Ptolemy.sum \
	  nest.sum \
	  pwhitake.sum \
	  starcharts.sum \
	  vergil01.sum \
	  vogel01.sum \
	  vthreads.sum \
	  yuhong01.sum


index.html : $(SOURCES) sum2html
	-chmod a+x sum2html
	sum2html $(SOURCES)
	-chgrp ptolemy *.html
	-chmod g+w *.html

clean:
	rm -f index.html
