# Akeeba Strapper

A handy distributions of namespaced jQuery and Bootstrap 2.3.4 for Joomla!

## Build instructions

### Prerequisites

In order to build the installation package of this library you need to have
the following tools:
* A command line environment. bash under Linux / Mac OS X works best. On Windows you will need to run most tools using an elevated privileges (administrator) command prompt.
* The PHP CLI binary in your path
* Command line Subversion and Git binaries(*)
* PEAR and Phing installed, with the Net_FTP and VersionControl_SVN PEAR packages installed

You will also need the following path structure on your system:
* `strapper` This repository, a.k.a. MAIN directory
* `buildfiles` [Akeeba Build Tools](https://github.com/akeeba/buildfiles)

### Initialising the repository

All of the following commands are to be run from the MAIN directory. Lines
starting with $ indicate a Mac OS X / Linux / other *NIX system commands. Lines
starting with > indicate Windows commands. The starting character ($ or >) MUST
NOT be typed!

1. You will first need to do the initial link with Akeeba Build Tools, running
   the following command (Mac OS X, Linux, other *NIX systems):

		$ php ../buildfiles/tools/link.php `pwd`

   or, on Windows:

		> php ../buildfiles/tools/link.php %CD%

1. After the initial linking takes place, go inside the build directory:

		$ cd build

   and run the link phing task:

		$ phing link

### Useful Phing tasks

All of the following commands are to be run from the MAIN/build directory.
Lines starting with $ indicate a Mac OS X / Linux / other *NIX system commands.
Lines starting with > indicate Windows commands. The starting character ($ or >)
MUST NOT be typed!

You are advised to NOT distribute the library installation packages you have built yourselves with your components. It
is best to only use the official library packages released by Akeeba Ltd.

1. Relinking internal files

   This is only required when the buildfiles change.

		$ phing link
		> phing link

1. Creating a dev release installation package

   This creates the installable ZIP packages of the component inside the
   MAIN/release directory.

		$ phing git
		> phing git


Please note that generated ZIP packages are written to the `release` directory inside the repository's root.
