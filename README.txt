FreeSSM
=======

FreeSSM is a free and easy to use diagnostic and adjustment tool for SUBARU®
vehicles. It currently supports the models LEGACY®, LIBERTY®, OUTBACK®, BAJA®,
IMPREZA®, FORESTER® and TRIBECA® starting with model year 1999 and provides
access to the engine and transmission control units.

PLEASE NOTE:
This program is NOT A PRODUCT OF FUJI HEAVY INDUSTRIES LTD. OR ANY SUBARU®-
ASSOCIATED COMPANY. It is a free reengineering project which is not contributed,
provided or supported by any company in any way.

All trademarks are property of Fuji Heavy Industries Ltd. or their respective
owners.

--------------------------------------------------------------------------------

0. TABLE OF CONTENTS:

   1. Licence
   2. Supported Platforms
   3. Requirements
   4. Compilation
   5. Installation
   6. Starting FreeSSM

--------------------------------------------------------------------------------

1. LICENCE:

This program is free software: you can redistribute it and/or modify it under
the terms of the GNU General Public License as published by the Free Software
Foundation, either version 3 of the License, or (at your option) any later
version.
You should have received a copy of the GNU General Public License along with
this program (see file LICENCE.txt). If not, see <http://www.gnu.org/licenses/>.

The use of this program is AT YOUR OWN RISK. The author is NOT LIABLE FOR ANY
EFFECTS caused by usage, including UNEXPECTED VEHICLE BEHAVIOR or DAMAGES.
This program is distributed in the hope that it will be useful, but WITHOUT ANY
WARRANTY; without even the implied warranty of FUNCTIONALITY ON YOUR VEHICLE,
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
See the GNU General Public License for more details.


TinyXML is released under the zlib license, see src/tinyxml/readme.txt and
www.sourceforge.net/projects/tinyxml for further informations.

--------------------------------------------------------------------------------

2. SUPPORTED PLATFORMS:

   - Linux/X11
   - Windows

With minor modifications, it should be possible to build FreeSSM on MacOS X
and other Unix systems, too, but there is currently no offical support.

--------------------------------------------------------------------------------

3. REQUIREMENTS:
   1.) FreeSSM source code (https://github.com/Comer352L/FreeSSM)
   2.) Qt framework (www.qt.io/download)
        Linux:   Qt4 (>= 4.4.0) or Qt5
                 Packages are usually available in the distribution repositories.
                 Development packages are needed.
        Windows: Qt5 (using MinGW, not MS Visual Studio)
                 Qt4 is not available for download anymore and the used MinGW
                 version is too old.
   3.) MinGW (only for MS Windows)
       MinGW is usually shipped with Qt and just needs to be selected during
       the installation process.
       However, in the past the installation process changed very often.
       There were times when it had to be downloaded and installed manually.
       Check mingw.org and sourceforge.net/projects/mingw in case you are forced
       to install it manually.

--------------------------------------------------------------------------------

4. COMPILATION:

Open a console window and switch to the FreeSSM-directory.

Preparation:
$ qmake
or (if you have Qt4 AND Qt5 installed)
$ qmake-qt4   or   $ qmake-qt5   (depending on your system environment)

Compilation:
$ make release
or
$ make debug

Translation files:
$ make translation

NOTE (Windows only): depending on the used Qt-version and system configuration,
                     'mingw32-make' must be called instead of 'make'.

--------------------------------------------------------------------------------

5. INSTALLATION:

$ make release-install
or
$ make debug-install

=> the application will be installed to 
	- Linux:	the users home-directory (/home/userXYZ/FreeSSM)
	- Windows:	C:\FreeSSM (can be moved after installation)

Uninstallation:

$ make release-uninstall
or
$ make debug-uninstall

--------------------------------------------------------------------------------

6. STARTING FreeSSM:

First, switch to the installation folder (see 5.).

Linux:
$ ./FreeSSM

Windows:
$ freessm

