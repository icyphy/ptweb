# $Id$

SOURCES = ptolemyII.sum \
		neuendor00.sum \
		neuendor00b.sum \
		tsaysummary.sum \
		corba00.sum \
		liuj00.sum \
		bilungNliuxj00.sum \
		yuhong00.sum \
		vogel00.sum

index.html : $(SOURCES) sum2html
	-chmod a+x sum2html
	sum2html $(SOURCES)
	-chgrp ptolemy *.html
	-chmod g+w *.html

clean:
	rm -f index.html
