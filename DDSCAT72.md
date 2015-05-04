This is a copy of the DDSCAT 7.2 main page which got obsolete on may 26, 2013.

# DDSCAT 7.2 #
Discrete Dipole Scattering (DDSCAT) is a Fortran code for calculating scattering and absorption of light by irregular particles and periodic arrangement of irregular particles. It has been jointly developed by
  * [Bruce T. Draine](http://en.wikipedia.org/wiki/Bruce_T._Draine) (Dept. of Astrophysical Sciences, Princeton University, draine@astro.princeton.edu) and
  * Piotr J. Flatau (Scripps Institution of Oceanography, University of California San Diego, pflatau@ucsd.edu).
The current version, DDSCAT 7.2.2 (released 2012 June 5), supersedes previous versions, which are no longer supported. (DDSCAT 7.2.0 was released 2012 February 16; DDSCAT 7.2.1 was released 2012 May 14).

  * DDSCAT 7.2 can calculate scattering and absorption by isolated particles (e.g., dust grains, ice crystals).
  * DDSCAT 7.2 can calculate scattering and absorption by periodic structures with applications to photonics and studies of arrays of nanostructures (for example absorption by periodic arrangement of finite cylinders, cubes, etc).
  * DDSCAT 7.2 offers capability for very fast near field calculation, as described in Flatau & Draine (2012).
  * DDSCAT 7.2 allows to display scattering targets, their composition, as well as scattering results using three dimensional graphical codes such as Paraview and Mayavi2 based on VTK format.
  * DDSCAT 7.2 provides an improved Windows distribution including fully native Windows binaries.
  * DDSCAT 7.2 provides conversion code between DDSCAT shape file format and VTK format.
  * DDSCAT 7.2 offers a new set of test examples.
  * DDSCAT 7.2 offers single and double precision options.

DDSCAT 7.2 is publicly available, and is now considered to be the standard version of DDSCAT. If you choose to use it, please send email to draine@astro.princeton.edu ''registering'' as a user; registered users of DDSCAT will be notified when updates to the code are made. As always, please let us know if you encounter problems downloading
DDSCAT, or if you have trouble using DDSCAT (but please read the
manual carefully before reporting problems!!).

DDSCAT 7.2 is gratis, subject to the GNU General Public License.  You may copy, distribute, and/or modify the software identified as under this agreement.  If you distribute copies of this software, you must give the recipients all the rights that you have.

However, if you use DDSCAT, we request that you reference some of the papers on which DDSCAT is based
  * Draine, B.T., & Flatau, P.J., "Discrete dipole approximation for scattering calculations", J. Opt. Soc. Am. A, 11, 1491-1499 (1994) (We check citations to this paper to track the overall DDSCAT use. On occasion we implement code improvements that way!)
  * Draine, B.T., & Flatau, P.J., "Discrete-dipole approximation for periodic targets: theory and tests", J. Opt. Soc. Am. A, 25, 2593-2703 (2008). (if you use this option of the code)
  * P. J. Flatau and B. T. Draine, "Fast near field calculations in the discrete dipole approximation for regular rectilinear grids," Opt. Express 20, 1247-1252 (2012) (if you use this option of the code)


## Downloading the DDSCAT 7.2 Code and Documentation ##
You can obtain a gzipped tarfile containing complete source code and documentation for DDSCAT 7.2, including programs DDSCAT (scattering calculations), CALLTARGET (target display and generation), READNF (near field 1dimensional and threed dimensional graphical display), VTRCONVERT (conversion of DDSCAT shape file to VTK format). An extensive User Guide is available. We provide some of our publications.  Windows executable version is also available.

To get full DDSCAT distribution begin with downloading the User Guide which we publish on arXiv.org. If you are using LINUX/UNIX operating system get the source code distribution. For this version you will need to compile the code. This offers opportunity to set the best compilation flags, MPI, Open-MP, etc. For Windows users we offer simple precompiled version; this is probably the fastest way to get started.

| File | Description | Notes |
|:-----|:------------|:------|
| [User Guide](http://arxiv.org/abs/1202.3424) | PDF file from arxiv | All users. Please read.|
| DDSCAT | Source including DDSCAT VTRCONVERT, CALLTARGET, READFN| Linux, MAC users|
| DDSCAT Windows | Windows native binary for 7.2.0| Windows users|
| Examples | DDSCAT examples| All users (includes tests and refractive index files)|
| Papers | Some of our DDSCAT related papers in PDF format| All users|

### Note on Windows version ###
For Windows users we offer simple precompiled version.  Notice that to run DDSCAT on Windows you need to know how to use command Window (you can not just "click" on ddscat.exe executable file). Such command window is opened using "cmd" command typed in start/run (it varies between Windows versions). Also notice that by default Windows operating system hides some files - that may influence your ability to "see" files such as ddscat.par. There are issues with certain releases of the Windows operating system in accessing > 2Gbyte of memory. These issues are not related in any way to DDSCAT implementation but rather are related to Windows operating system. Therefore, one may find using LINUX operating system as more viable option for large DDSCAT runs.

### Building DDSCAT ###
A single distribution is provided for DDSCAT 7.2 -- by appropriate editing of the Makefile, this distribution can be used to generate programs using either single- or double-precision; either without or with MPI capability; either without or with OPENMPI support; and either without or with the Intel MKL library.

Note: DDSCAT 7.2 has been extensively tested in single-processor mode. However, it has received only limited testing with MPI and OpenMP, and it is possible that some of the changes to the code in the 7.1 -> 7.2 transition might lead to OpenMP or MPI problems.  If you are a user of MPI and/or OpenMP, please run some test calculations in both single-processor and multiprocessor mode, and compare results, before doing any "production" calculations with MPI and/or OpenMP.  If you do such tests, we would appreciate being informed of the outcome.

## Previous versions ##

Past versions of the DDSCAT are still available but we prefer to maintain only the most recent version of the code. For example version 6 is [available](http://www.astro.princeton.edu/~draine/DDSCAT.6.0.html).

Version 7.1 is no longer supported, although it will continue to be available. If you have been using Version 7.1, please switch to Version 7.2.
| File | Description | Notes |
|:-----|:------------|:------|
| [Documentation (old)](http://arxiv.org/abs/1002.1505v1) | DDSCAT documentation | PDF, postscript |
| [DDSCAT.tgz (old)](http://ddscat.googlecode.com/files/ddscat7.1.0_100303.tgz) | DDSCAT source version (tarred and zipped)| full version of DDSCAT; needs to be compiled |