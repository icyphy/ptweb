#SOURCES =	/users/sedwards/berkeley/sedwards97a.sum \
#		/users/bilung/Papers/ERL/97 \
#		/users/dstevens/rsch_abstract \
#		/users/girault/Articles/erl-sum-97.html \
#		/users/seehyun/doc/ptolemy/seehyun97a.sum

SOURCES = sedwards97a.sum cameron97a.sum bilung97a.sum dstevens97a.sum \
	girault97a.sum seehyun97a.sum johnr97a.sum eal97a.sum eal97b.sum \
	galicia97a.sum michaelg97a.sum

index.html : $(SOURCES) sum2html
	-chmod a+x sum2html
	sum2html $(SOURCES)
	-chmod g+w *.html

clean:
	rm -f index.html
