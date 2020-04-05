# zlib-x86_x64
Native Visual Studio project files to compile in Windows x86/x64/Debug/Release

# Background #
zlib has excellent support for compiling in Visual Studio, if only a
little outdated. But the files provided can easily be converted to
work with the latest VS (I use VS 2019 Community Edition).

However, the defaults chosen are slightly different from those I use
in my projects and thus, I present a slightly modified (apart from the
upgrade to the 2019 format) solution/project files.

The main changes are in the OutDir and IntDir locations, which follow
a standard that allows these projects to work as subprojects of other
projects that use this library. In fact, zlib is one of the base
libraries that is used by almost all other libraries that I use for my
program. Other changes are to produce static libraries, use the DLL
CRT for both Debug/Release.

# Installation/Usage #
  * git clone [zlib, tested w/ v1.2.11](https://github.com/madler/zlib.git). I switch the tree to the v1.2.11 tag afterward.
  * git clone [zlib-x86_x64](https://github.com/sridharb1/zlib-x86_x64) into another folder.
  * Copy the contents of this folder into the contrib/vstudio folder
    of the zlib repository. Thus, the vc14 folder of zlib-x86_x64
    should overwrite the same in zlib.
  * Use zlibvc.sln to compile.
