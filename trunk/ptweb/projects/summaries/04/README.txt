I did the heavy lifting

I copied the summaries over from laster year, they are visible at
http://ptolemy.eecs.berkeley.edu/projects/summaries/04/index.html
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

4. In your summary, consider adding the following
   
   * GIF screenshots are nice.

   * If there is a website that talks about your research, then
   consider adding a link to the bottom (before the references) that
   looks something like:
     For more information about Foo, see 
     <a href="http://ptolemy.eecs.berkeley.edu/projects/foo/index.htm" 
          target="_top"><code>http://ptolemy.eecs.berkeley.edu/projects/foo/</code></a>

   There are several reasons for this:
   1. The reader might want more info
   2. Spelling out the URL ensures that it will be in the printed
   version of the Research Summary (we should check out previous years
   and see what happens to URLS)
   3. target="_top" means that the page will come up outside the
   current frame.  This is critical if the link goes to a frame
   based webpage

   
   * Any references to pertinent papers.  Be sure to use
   proper bibliographic format - your best bet is to copy the reference
   from http://ptolemy.eecs.berkeley.edu/publications/papers
   Usually once does not use target="_top" here, though you can if
   you want

5. Spell check your summary with ptspell

6. update the .html files
   make

7. Check in your changed sum file (and makefile if necessary)
   cvs commit -m "Added my research" yourfile.sum makefile

8. Become the ptII user on messier, see
   http://www.gigascale.org/ptolemy/group/public.htm

   Once you are set up, use ssh to log on to a Unix machine such
   as cooley, then do
   ssh -l ptII messier
   cd ~ptII/ptweb/projects/summaries/03
   cvs update
   make
	
9.  Verify your changes
http://ptolemy.eecs.berkeley.edu/projects/summaries/03/index.html   


--------
