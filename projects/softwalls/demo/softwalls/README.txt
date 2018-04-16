$Id: README.txt 93 2004-01-14 01:40:00Z cxh $
This model uses compressed data files from surfacesCompressed.jar

surfacesCompressed.jar is not checked in to cvs, it is 3.5Mb in size.
You can download it from the website
http://softwalls.eecs.berkeley.edu/demo/softwalls/surfacesCompressed.jar
See below for information about how to manipulate the data files.

The Ptolemy jar files are not checked in either.  You can copy them
with
(cd $PTII/ptolemy/apps/softwalls; cvs update; make install) 
(cd $PTII; tar -cf - lib/diva.jar ptolemy/apps/softwalls/softwalls.jar ptolemy/domains/ct/ct.jar ptolemy/domains/fsm/fsm.jar ptolemy/domains/gr/gr.jar ptolemy/ptsupport.jar ptolemy/vergil/vergilApplet.jar ) | tar -xf -


Data Files
----------
The master copy of the model is in the softwalls repository at
softwalls/ptolemy/softwallsSimulator/fixedTime.xml

That directory also contains the uncompressed data files in the
surfaces/ subdirectory

To dump out the uncompressed data from the model used by the applet,
use the expert writeOutData parameter of the ImplicitSurfaces actor:

1. vergil softwalls.xml
2. Look inside the "Control Surfaces"  composite actor
3. Look inside the "ImplicitSurface" composite actor
4. Double click on the ImplicitSurface actor and select Preferences ->
expert Mode and Ok
5. In the ImplicitSurfaces Edit Parameters window, select writeOutData.
6. Run the model
7. The uncompressed data will appear in the surfaces/ subdirectory.

Note that the ImplicitSurfaces actor has a filesAreCompressed parameter.
Initially, this parameter is set to true so that we are reading in 
compressed files from surfacesCompressed.jar, which is found in the classpath
of the applet.

To update the compressed data:
1. Set the filesAreCompressed parameter to false
2. Set the writeOutData parameter to true
3. Place the uncompressed data in the surfaces directory
4. Run the model
5. The compressed data will be generated.

To generate the applets, I used the following command

$PTII/bin/copernicus -verbose -codeGenerator applet \
 -ptIIUserDirectory c:/cxh/src/softwallsweb/demo/softwalls
 -targetPackage softwalls \
 -targetPath softwalls \
 -outputDirectory softwalls \
 softwalls.xml

This will generate new applets in a softwalls subdirectory and 
copy over the appropriate jar files.

You would also need to copy surfacesCompressed.jar in
and update the classpath in the applets.


Running the model by hand
-------------------------
Under Cygwin bash, to run the model inside vergil:
  CLASSPATH=surfacesCompressed.jar
  export CLASSPATH
  vergil softwalls.xml
