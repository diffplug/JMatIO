# Migrate to [MatFileRW](https://github.com/diffplug/matfilerw)

Since JMatIO wasn't updated for a while, lots of people made forks.  This fork includes several improvements, but all the packages were renamed to `ca.mjdsystems.jmatio`, which makes it incompatible with other JMatIO forks.

[MatFileRW](https://github.com/diffplug/matfilerw) is an actively maintained fork of JMatIO which merges the improvements of several different forks (including this one).

If you want to adopt the improvements of other branches, while also keeping the features of this branch, you should download `com.diffplug.matsim:matfilerw:2.0.0.TRANSITION` from mavenCentral.  This contains the `ca.mjdsystems.jmatio` packages unchanged, but marked as deprecated.  After you have removed all dependencies on the `ca.mjdsystems.jmatio` packages, you will be able to use the regular `2.0.0` version, and its descendants.

### Old header

JMatIO is a JAVA library to read/write/manipulate with Matlab binary
MAT-files.

If you would like to comment, improve, critisize the project please 
email me: wgradkowski@gmail.com 

or visit JMatIO project page at Sourceforge:
http://www.sourceforge.net/projects/jmatio

Subversion Access

This project's SourceForge.net Subversion repository can be checked out through 
SVN with the following instruction set:

svn co https://jmatio.svn.sourceforge.net/svnroot/jmatio/trunk jmatio 

Have fun :)

Wojciech Gradkowski

CHANGE LOG:
[09.05.2013]
+ added read/write support for input/output streams (ss, jsh)

[04.12.2012]
+ adding various fixes (thanks to: Kristofer Sandlund)
+ adding read support for objects, java objects, other types
+ performance enhancements

[05.10.2007]
+ Sparse matrix bugfixes by Jonas Pettersson (LU/EAB)
+ MatFileReader performance enhancements by Eugene Rudoy
+ new MatFileReader methods added

[02.03.2007]
+ Regression bug fixed: Double arrays created natively in Matlab are read 
  incorrectly (reversed byte ordering)

[22.02.2007]
+ Added support:UInt8 array 
+ MAJOR reading performance enhancement - reading is as fast as in Matlab now
+ Removed Log4j references

TODO:
- Other array types (serialized objects (OPAQUE) is done partially)
- Writer performance enhancement
- Documentation and examples
- Organize JUnit tests
- Refactor exceptions
- Make structures and cell arrays more user friendly

NOTE:
Numerical arrays (MLDouble, MLUint8) are now backed by direct ByteBuffers. For 
really BIG arrays the maximum heap size for direct buffers may be modified by 
-XX:MaxDirectMemorySize=<size>


[some.time.2006]
Currently supproted data types are:
+ Double array
+ Char array
+ Structure
+ Cell array
+ Sparase array

