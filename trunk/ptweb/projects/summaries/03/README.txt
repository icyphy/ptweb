I did the heavy lifting

I copied the summaries over from laster year, they are visible at
http://ptolemy.eecs.berkeley.edu/projects/summaries/03/index.html
but there are no links from the website to them yet.

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
http://ptolemy.eecs.berkeley.edu/projects/summaries/03/index.html   


--------
