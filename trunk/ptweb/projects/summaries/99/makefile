# $Id$

SOURCES = eal98b.sum bilungNliuxj99.sum galicia98a.sum davisj99a.sum lmuliadi99a.sum mudit99a.sum neuendor99.sum nsmyth99a.sum tycho.sum ptolemyII.sum liuj99.sum yuhong99.sum wbwu99a.sum wbwu99b.sum

index.html : $(SOURCES) sum2html
	-chmod a+x sum2html
	sum2html $(SOURCES)
	-chgrp ptolemy *.html
	-chmod g+w *.html

clean:
	rm -f index.html
