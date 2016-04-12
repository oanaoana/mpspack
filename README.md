# MPSpack : 2D Helmholtz scattering and eigenvalue problems via particular solutions and integral equations

### Alex Barnett 4/12/16.  Version 1.4

MPSpack is a user-friendly and fully object-oriented MATLAB toolbox
that implements the method of particular solutions, nonpolynomial FEM,
the method of fundamental solutions, and integral equation methods,
for the efficient and highly accurate solution of Laplace eigenvalue
problems, interior/exterior Helmholtz boundary-value problems
(e.g. wave scattering), periodic diffraction problems, and related PDE
problems, on piecewise-homogeneous 2D domains.

Version 1.0 was released in 2009. Since then it has settled into a
repository for a variety of new numerical methods developed for corner
domains, periodic problems, and high-frequency Dirichlet and Neumann
eigenvalue problems.  It is stable and will not have much future
development. Instead I expect to release a replacement package for integral
equations.

*This work was supported by the National Science Foundation under
grants DMS-0811005 and DMS-1216656, and Engineering and Physical
Sciences Research Council Grant EP/H00409/1. It includes codes by
V. Rokhlin, A. Pataki, Z. Gimbutas, S. Hawkins, and several others.*

## Requirements

* MATLAB 2008a or newer (in particular, no toolboxes needed)

* Optional requirements for advanced features (see `doc/manual.pdf`):
..* [FMMLIB2D](http://www.cims.nyu.edu/cmcl/fmm2dlib/fmm2dlib.html)
..* [LP2D](https://math.dartmouth.edu/~ahb/software/lp2d.tgz)
..* GNU Scientific Library [GSL](http://www.gnu.org/software/gsl)

## Installation

Install `git`. Eg on an ubuntu/debian
linux system use `sudo apt-get install git`. Then
`git clone https://github.com/ahbarnett/mpspack`
will create the directory `mpspack` containing the package.

In MATLAB, type `addpath /path/to/mpspack`. See Usage below to test your
installation.

Add the above `addpath` command to your MATLAB `startup.m` file if you
want the MPSpack toolbox available by default.

*Note a [snapshot](https://code.google.com/archive/p/mpspack/)
of version 1.33 from 2014 remains archived on the sadly-defunct `googlecode`.
*


## Usage

To test your installation:
in MATLAB make sure you're in the `mpspack` top directory and type
`run test/testdielscatrokh` which should take about 1 second to run
and produce a wave scattering figure from a smooth dielectric domain,
along with a pointwise error, which should be small (ie less than 1e-14).

See `doc/tutorial.pdf` and `doc/manual.pdf` for detailed examples and usage.


## To do list

* Extract the best quadrature schemes for a new BIE2D package

* Interpolation to replace Zp, Zpp for convenience but losing digits

