This directory consists of the files necessary to use SSH and CVS on a NT box.

Finishing the Installation
--------------------------
To finish the installation, you will need to:

1. Create ~/.ssh/identity and ~/.ssh/identity.pub on the UNIX machine.
   (The steps below are from John Reekie's cvs.html page)
   1. On a Unix machine, generate your RSA encryption keys: 
            ssh-keygen
      Enter a passphrase when prompted. This will generate the files 
      ~/.ssh/identity and ~/.ssh/identity.pub, which
      are your private and public encryption keys respectively. 

   2. To use ssh between two unix machines, copy ~/.ssh/identity.pub 
      on the local machine to ~/.ssh/authorized_keys 
      on the remote machine. If you're just testing this and have a shared 
      file-system, then of course this is the same directory. 

     

2. Copy ~/.ssh/identity and ~/.ssh/identity.pub from the Unix machine to
   the directory $HOME/.ssh on the Windows machine

   You may be able to use the scp binary to copy the files.  Under Cygwin bash:
	mkdir $HOME/.ssh
	scp yourunixmachine:~/.ssh/identity $HOME/.ssh
	chmod 600 identity
	scp yourunixmachine:~/.ssh/identity.pub $HOME/.ssh

   When scp prompts you for a password, use your Unix account password.

3. Test the ssh works:
	ssh -v yourunixmachine date
   SSH should prompt you for your RSA key that you used when you ran ssh-keygen above.

4. To test CVS, start up a MSDOS shell or Cygwin bash and type
     cvs checkout yourpackage
   where 'yourpackage' is the name of the package you are trying to check out.


Using .rhosts and RSA authentication
------------------------------------
The above setup will prompt you for your password each time you run a cvs command.
If you set up RSA authentication, then you won't need to type your password each time.

Note that this means that if someone steals your laptop and breaks into your account,
they will be able to use the ssh command to get on to your Unix account.

1. On your Unix account, create the file ~/.srhosts, and add your Windows machine name
   to it.

2. On the Windows machine, copy c:/etc/ssh/ssh_host_key.pub to a temporary file
   on the Unix machine.  If you use scp here, note that scp does not understand the
   Windows c: naming convention, it think c: is a machine named 'c'.  To copy the file,
   try something like
	cd c:/etc/ssh
	scp ssh_host_key.pub yourunixmachine:/tmp

3. On the unix machine grab the contents of the copy of ssh_host_key.pub that
   you copied over, and place it in your $HOME/.ssh/known_hosts file.
   Remove the windows machine name from the end of the line and place it at the
   beginning.  You should end up with something like
	mowat.eecs.berkeley.edu 1024 17 2734812436871248921436987214872164987243
   Where the last number is several lines long.

4. Test ssh with
	ssh -v yourunixmachine date
   You should not have to type in your password



Troubleshooting CVS SSH under NT
--------------------------------

   1.Run 'ssh -v yourunixmachine date' and check the output.

   2.Check the value of the CVSROOT environment variable.  It should be something like:
	:ext:carson.eecs.berkeley.edu:/users/cvs/Repository
 
   3.Be sure that you have created a key on the Unix side and 
     copied the identity* files from Unix to NT 

   4.Be sure that $HOME is set for your NT account 

   5.Try using the ssh.exe binary that the $CVS_RSH variable refers to. 

     Below is an example where we rsh over to carson and get the date: 

     bash-2.02$ echo $CVS_RSH
     D:\Program Files\Ptolemy\CVS SSH\ssh.exe
     bash-2.02$ /Program\ Files/Ptolemy/CVS\ SSH/ssh carson date
     Enter passphrase for RSA key 'cxh@carson.eecs.berkeley.edu':
     ld.so.1: /usr/local/bin/xauth: warning: /usr/4lib/libXmu.so.4.0: has older revision than expected 10
     Thu Feb  4 15:35:06 PST 1999

     Below is an example that failed because of an incorrect CVS password, note that the password is prompted
     for twice: 

     bash-2.02$ /Program\ Files/Ptolemy/CVS\ SSH/ssh carson date
     Enter passphrase for RSA key 'cxh@carson.eecs.berkeley.edu':
     Bad passphrase.
     Password:
     Permission denied.
     bash-2.02$

   6. Verify that you can use ssh to connect between two Unix boxes.

   7. Reboot NT.

Bugs
----
* The ssh that is shipped is very old and has known security holes.  Since we are
using only the client, the risk is lessened, but if you are concerned about security,
you may want to look elsewhere.


Acknowledgments
---------------

cvs came from
	http://download.cyclic.com/pub/cvs-1.10.5/
with a patch from
	http://bmrc.berkeley.edu/people/chaffee/winntutil.html#sshnt

ssh came from
	ftp://ftp.cs.hut.fi/pub/ssh/contrib/ssh-1.2.14-win32bin.zip

cvs.html was written by John Reekie, the original page is at:
	http://ptolemy.eecs.berkeley.edu/~johnr/info/cvs.html

The home page for this package is
	http://ptolemy.eecs.berkeley.edu/cvsdoc


