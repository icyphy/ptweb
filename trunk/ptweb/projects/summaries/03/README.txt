I did the heavy lifting
I copied the summaries over from laster year, they are visible at
http://ptolemy.eecs.berkeley.edu/projects/summaries/03/index.html
but there are no links from the website to them yet.

We need someone to coordinate this.

Each person should have a summary, so either create up or update your
summary.

To do this,
1. Check out a copy of the website
   cvs -d :ext:cooley.eecs.berkeley.edu:/users/cvs/Repository co ptweb
2. go to ptweb/projects/summaries/03

3. If your .sum file exists, updatit
   if it does not exist, copy an existing one, add it it to the
   makefile and run
   cvs add yourfile.sum

4. update the .html files
   make

5.  Check in your changed sum file (and makefile if necessary)
    cvs commit -m "Added my research" yourfile.sum makefile

6. Become the ptII user on messier, see
   http://www.gigascale.org/ptolemy/group/public.htm

   Once you are set up, use ssh to log on to a Unix machine such
   as cooley, then do
   ssh -l ptII messier
   cd ~ptII/ptweb/projects/summaries/03
   cvs update
   make
	
7.  Verify your changes
http://ptolemy.eecs.berkeley.edu/projects/summaries/02/index.html   


--------

    
    I need someone to coordinate this...
    volunteers?
    
    Edward
    
    >Date: Mon, 24 Sep 2001 14:00:34 -0700 (PDT)
    >From: Cassandra Dunn <cassie@EECS.Berkeley.EDU>
    >To: eecs-profs@EECS.Berkeley.EDU
    >Subject: Research Summary abstracts
    >
    >Professor:
    >
    >Please submit your abstracts (and encourage your students
    >and researchers to) for the 2002 EECS/ERL Research Summary
    >by November 16th. To submit one, go to:
    >http://www.eecs.berkeley.edu/IRO/Summary/submit.html
    >
    >Please remind your students that abstracts should be 200
    >words or less, with links to other research related web
    >pages if necessary. We accept EPS and GIF figures.
    >
    >2001 Research Summary abstracts can be found at:
    >http://www.eecs.berkeley.edu/IRO/Summary/01abstracts
    >
    >I have also sent email to all grad students about this.
    >If you have any questions, feel free to contact me.
    >
    >Cassie Dunn
    >203 Cory
    >3-6684
    
    ------------
    Edward A. Lee, Professor
    518 Cory Hall, UC Berkeley, Berkeley, CA 94720
    phone: 510-642-0455, fax: 510-642-2739
    eal@eecs.Berkeley.EDU, http://ptolemy.eecs.berkeley.edu/~eal
--------
