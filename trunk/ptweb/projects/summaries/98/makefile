# @(#)makefile	1.8 10/23/97
# Last year's files
#SOURCES = sedwards97a.sum cameron97a.sum bilung97a.sum dstevens97a.sum \
#	girault97a.sum seehyun97a.sum johnr97a.sum eal97a.sum eal97b.sum \
#	galicia97a.sum michaelg97a.sum

SOURCES = eal98b.sum bilung98a.sum galicia98a.sum cameron98a.sum davisj98a.sum mudit98a.sum tycho.sum

index.html : $(SOURCES) sum2html
	-chmod a+x sum2html
	sum2html $(SOURCES)
	-chgrp ptolemy *.html
	-chmod g+w *.html

clean:
	rm -f index.html
