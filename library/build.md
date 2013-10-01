---
layout: page
title: Build Instruction
description: ""
---

## Linux / Mac OS X
First, obtain the source code from the repository using Git. To simply download the code, run the following command from a terminal:

    $ git clone https://github.com/openigtlink/OpenIGTLink.git

Then configure using CMake. The library requires CMake version higher than 2.4.

    $ mkdir OpenIGTLink-build
    $ cd OpenIGTLink-build
    $ cmake -DBUILD_EXAMPLES:BOOL=ON ../OpenIGTLink
    $ make

You may install the library into your disk (optional). The default target directory is /usr/local, but you can configure it from the CMake configuration screen. To install the files, run

    $ make install

You might need super user access.

## Sun OS

For Sun OS (Solaris), you may follow the instruction for Linux/Mac OS X described above. If you want to explicitly specify Sun CC instead of GNU CC, options for cmake look like:

    cmake -DCMAKE_C_COMPILER:STRING=/opt/SUNWspro/bin/cc -DCMAKE_CXX_COMPILER:STRING=/opt/SUNWspro/bin/CC -DBUILD_EXAMPLES:BOOL=ON ../OpenIGTLink

## Windows
* Download Git Windows client, if you don't have one already
* You will also need [CMake](http://www.cmake.org/HTML/Download.html) and a C/C++ compiler as [Microsoft Visual C++](http://www.microsoft.com/express/vc/)
* Download the source code from Git repository.
  * URL of repository: git://github.com/openigtlink/OpenIGTLink.git
  * Click OK
* Run CMake
  * Where is the source code: C:\Devel\OpenIGT\OpenIGTLink
  * Where to build the binaries: C:\Devel\OpenIGT\OpenIGTLink-build
  * Click "Configure" and select your compiler (usually just click "OK")
  * Message: "Build directory does not exit, should I create it?" - click "OK"
  * Click "Configure"
  * Click "OK" to close CMake
* Start Visual C and compile the project (C:\Devel\OpenIGT\OpenIGTLink-build\OpenIGTLink.sln)
If all went OK you will have the executable and the library:
* C:\Devel\OpenIGT\OpenIGTLink-build\bin\debug\igtlSocketTest.exe
* C:\Devel\OpenIGT\OpenIGTLink-build\bin\debug\OpenIGTLink.lib

## Note on Windows
If you are planning to link the OpenIGTLink Library with IGSTK, or the 3D Slicer OpenIGTLinkIF module, please make sure that you use the Windows version of CMake (not the one contained in the Cygwin environment) and Visual Studio 2008. Since IGSTK and 3D Slicer are compiled with Visual Studio, the OpenIGTLink library built in cygwin environment using GCC cannot be linked with those software.

## iOS (iPhone and iPod)
NOTE: OpenIGTLinkIF is tested on iOS with the following condition:
    Target: iOS 5.0.1
    Host: Mac OS X 10.7.2 with Xcode 4.2
    CMake: 2.8.6
    OpenIGTLink: git@github.com:openigtlink/OpenIGTLink.git (commit 68e903965f3f2dde8c0303f6c41cdc81a68d28f4)

Suppose we have a copy of the OpenIGTLink source files in IGTL_SOURCE_DIR and will build the library in IGTL_BINARY_DIR.
First, create a XCode project with CMake:

    cd IGTL_BINARY_DIR
    ccmake -GXcode IGTL_SOURCE_DIR

No option needs to be edited in the ccmake interface. Simply press 'c' twice and then 'g' to generate a project file and other necessary files for XCode.

Once the files are generated, open "OpenIGTLink.xcodeproj" from XCode. Before building OpenIGTLink for iOS, we generate binary for Mac OS X.
At the left-top of XCode window, choose "OpenIGTLink > My Mac 64-bit" as a target from a pull down-menu and press "Run" just next to the pull-down. If everything goes well, the status window at the center of the window top shows "Build ALL_BUILD: Succeeded."

<img src="http://www.na-mic.org/Wiki/images/1/1b/OpenIGTLink_Library_Build_iOS_1.png"/>

The next step is to build a binary for iOS simulator. Choose "OpenIGTLink" from "PROJECT" column and change Base SDK to "iOS 5"  in Build settings.

<img src="http://www.na-mic.org/Wiki/images/b/b6/OpenIGTLink_Library_Build_iOS_2.png" width="600"/>

<img src="http://www.na-mic.org/Wiki/images/6/6a/OpenIGTLink_Library_Build_iOS_3.png" width="600"/>

After making sure that the target is set to "OpenIGTLink > iPhone 5.0 Simulator," press run button to start compilation process. If everything goes well, the binary file "libOpenIGTLink.a" is stored in IGTL_BINARY_DIR/bin/Debug. It may be a good idea to change the name of "Debug" directory to something like "Sim5.0Debug", since you will need to have also a binary for actual device and switch between two binaries (or four binaries if you build Release version as well).

To use the binary file from your iPhone program, specify the following directories as "Header Search Path":
* IGTL_SOURCE_DIR/Source
* IGTL_SOURCE_DIR/Source/igtlutil
* IGTL_BINARY_DIR/
Also, add the binary file ("libOpenIGTLink.a") under a new group "OpenIGTLink" in the navigation area in on the left of XCode Window.

<img src="http://www.na-mic.org/Wiki/images/9/9a/OpenIGTLink_Library_Build_iOS_4.png"/>


Reference
* Shabash B, Hamarneh G, Huang ZF, Ibanez L, ITK on the iOS, http://www.sfu.ca/~zfh/IJ_755_1_BuildingITKinTheiPhone.pdf



