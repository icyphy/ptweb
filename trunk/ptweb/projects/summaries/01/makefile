# $Id$
OLDSOURCES = ptolemyII.sum \
		moml.sum \
		neuendor00.sum \
		neuendor00b.sum \
		tsaysummary.sum \
		corba00.sum \
		liuj00.sum \
		bilungNliuxj00.sum \
		yuhong00.sum \
		kienhuis00a.sum \
		kienhuis00b.sum \
		vogel00.sum \
		vissers00.sum \
		softpract00.sum

SOURCES = ptolemyII.sum \
	  cont_and_disc.sum \
	  e_Ptolemy.sum \
	  nest.sum

index.html : $(SOURCES) sum2html
	-chmod a+x sum2html
	sum2html $(SOURCES)
	-chgrp ptolemy *.html
	-chmod g+w *.html

clean:
	rm -f index.html
