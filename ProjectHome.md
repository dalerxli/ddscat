# NOTE: New DDSCAT site #
In March of 2015 GOOGLE announced that it will discontinue their code distribution service. Therefore we are migrating DDSCAT to our new site
http://www.ddscat.org



## DDSCAT Introduction ##


Discrete Dipole Scattering (DDSCAT) is a Fortran code for calculating scattering and absorption of light by irregular particles and periodic arrangement of irregular particles. It has been jointly developed by
  * [Bruce T. Draine](http://en.wikipedia.org/wiki/Bruce_T._Draine) Department of Astrophysical Sciences, Princeton University, draine@astro.princeton.edu) and
  * Piotr J. Flatau Scripps Institution of Oceanography, University of California San Diego, pflatau@ucsd.edu
The current version, DDSCAT 7.3.0 (released 2013 May 26), supersedes previous versions, which are no longer supported.

DDSCAT  [User Guide 7.3 is available.](https://www.dropbox.com/s/n2mgrkx3tqqir39/ddscat7.3.0_UserGuide_130529.pdf?dl=0)

  * DDSCAT can calculate scattering and absorption by isolated particles (e.g., dust grains, ice crystals).
  * DDSCAT can calculate scattering and absorption by periodic structures with applications to photonics and studies of arrays of nanostructures (for example absorption by periodic arrangement of finite cylinders, cubes, etc).
  * DDSCAT offers capability for very fast near field calculation

DDSCAT 7.3 differs from DDSCAT 7.2 by offering these options:

  * DDSCAT 7.3.0 includes the "Filtered Coupled Dipole" method as an option
  * DDSCAT 7.3.0 can now efficiently calculate both E and B throughout a user-specified rectangular volume containing the target.  The polarization P, and nearfield E (and B, if desired) are saved as files.
  * DDSCAT 7.3.0 now reports the macroscopic E field within the target, rather than the "microscopic" E field as in the past.
  * The DDSCAT 7.3.0 distribution includes a separate F90 code, DDPOSTPROCESS.f90, designed to read the stored P and E (and B) and perform postprocessing calculations (e.g., calculating the Poynting flux).  DDPOSTPROCESS.f90 can be modified by the user to do additional postprocessing calculations, or to output results in other formats.
  * As with DDSCAT 7.2.2, the DDSCAT 7.3.0 distribution includes VTRCONVERT.f90 to support visualization of the target geometry using the Visualization Toolkit
  * There are new versions of the conjugate gradient solvers

DDSCAT 7.3.0 is publicly available, and is now considered to be the standard version of DDSCAT. If you choose to use it, please send email to **draine@astro.princeton.edu** ''registering'' as a user; registered users of DDSCAT will be notified when updates to the code are made. As always, please let us know if you encounter problems downloading DDSCAT, or if you have trouble using DDSCAT (but please read the manual carefully before reporting problems!)

DDSCAT 7.3 is gratis, subject to the GNU General Public License.  You may copy, distribute, and/or modify the software identified as under this agreement.  If you distribute copies of this software, you must give the recipients all the rights that you have.

However, if you use DDSCAT, we request that you reference some of the papers on which DDSCAT is based
  * [Review paper is available from J. Opt. Soc. Am. site.](http://www.opticsinfobase.org/josaa/abstract.cfm?uri=josaa-11-4-1491) Draine, B.T., & Flatau, P.J., "Discrete dipole approximation for scattering calculations", J. Opt. Soc. Am. A, 11, 1491-1499 (1994) (we check citations to this paper to track the overall DDSCAT use; on occasion we implement code improvements that way!)
  * Draine, B.T., & Flatau, P.J., "Discrete-dipole approximation for periodic targets: theory and tests", J. Opt. Soc. Am. A, 25, 2593-2703 (2008). (if you use this option of the code)
  * P. J. Flatau and B. T. Draine, "Fast near field calculations in the discrete dipole approximation for regular rectilinear grids," Opt. Express 20, 1247-1252 (2012) (if you use this option of the code)
  * P. J. Flatau and B. T. Draine, "Light scattering by hexagonal columns in the discrete dipole approximation," Opt. Express  22, 21834-21846 (2014).

**Out preference is that you do not reference the DDSCAT User Guide (there are too many releases of this document)**

## Downloading the DDSCAT 7.3 Code and Documentation ##
You can obtain a gzipped tarfile containing complete source code and documentation for DDSCAT 7.3. To get full DDSCAT distribution begin with downloading the User Guide. If you are using LINUX/UNIX operating system get the source code distribution. For this version you will need to compile the code. This offers opportunity to set the best compilation flags, MPI, Open-MP, etc. For Windows users we offer simple precompiled version; this is probably the fastest way to get started but also somewhat limited in ability to make source code changes. Really large DDSCAT runs should probably be done on 64-bit UNIX/LINUX.



## Note on Windows version ##
For Windows 7.3 users we offer  precompiled (using gfortran) 32-bit and 64-bit versions.  Notice that to run DDSCAT on Windows you need to know how to use a "command window" (there is no graphical interface). We suggest that users install MinGW and use MinGW shell window (optional). Also notice that by default Windows operating system hides some files - that may influence your ability to "see" files extensions such as ddscat.par. Current executables were done using 32bit MinGW and 64bit MinGW. Using OpenMP and MKL libraries (Intel compiler) the code will run 3-4 times faster but we currently do not provide such binaries. For large problems with, say one milion of dipoles or more, you will run into 2Gbyte memory limit if you are using a 32-bit computer. To solve this problem on both Windows and Linux move to a 64-bit operating system and use 64-bit compilers. You may also run into stack size limitation when running the code with OpenMP. In such case try
  * ulimit -s unlimited
See also [this link](http://code.google.com/p/ddscat/wiki/Windows).


## User codes ##
These codes are provided by users of DDSCAT and are not supported by Draine/Flatau.

**We welcome Users to provide additional public domain codes.**

| File | Description |
|:-----|:------------|
| [ddaconvert](https://code.google.com/p/ddscat/downloads/detail?name=ddaconvert-r17.tar.gz) | R. Schuh, Arbitrary particle shape modeling in DDSCAT and validation of simulation results, in Proceedings of the DDA-Workshop, T. Wriedt and A. G. Hoekstra, Eds., pp. 22–24, Bremen, Germany (2007) |
| [DDSCAT-mu](https://code.google.com/p/ddscat/downloads/detail?name=DDSCAT-mu%20.zip&can=2&q=#makechanges) | Yu You, George W. Kattawar, Peng-Wang Zhai, and Ping Yang, "Zero-backscatter cloak for aspherical particles using a generalized DDA formalism," Opt. Express 16, 2068-2079 (2008)|
| [ddscatcpp](https://code.google.com/p/ddscatcpp/) | DDSCAT 7.3 written in C++  V.Choliy (2013)|
| [shape tools](https://github.com/feranick/ddscat-tools) | shape utilities by Nicola Ferralis (September 2013)|