# of230-patches
Some patches for compiling OpenFOAM-2.3.0 on modern compilers (created on/for Ubuntu >= 16.04). Applying the patch solves compilation errors due to `int yyFlexLexer::yywrap()`, fixes the compilation of ensightPart (and libraries linked to it) due to missing `isnan`, and imposes a modification of the bashrc file to use the system-wide openmpi libraries.

## Installation
* Unpack the source and ThirdParty as explained on the OpenFOAM website: https://openfoam.org/download/2-3-0-source/
* In the terminal, go to the OpenFOAM-2.3.0 source folder:
  `cd ~/OpenFOAM/OpenFOAM-2.3.0`
* Clone the patch file:
  `git clone https://github.com/iroghair/of230-patches.git`
* Apply the patch file:
  `patch -p0 < of230-patches/of230.patch`
* Continue with the OpenFOAM compilation:
  `./Allwmake`


