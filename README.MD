# PuTTYNG

This is a modified version of [PuTTY](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html) from [Simon Tatham](https://www.chiark.greenend.org.uk/~sgtatham/) to be used with [mRemoteNG](https://mremoteng.org/).

This version removes the "Connection lost" popup and just writes a message to the terminal. 

IE:
------------------- PuTTYNG Fatal Error ------------------
- Network error: Software caused connection abort


**The following files within the project were modified:**
- BE_ALL_S.C
- CMDLINE.C
- PUTTY.H
- WINDOWS/PUTTY.RC
- WINDOWS/VERSION.RC2 
- WINDOWS/WINDOW.C

**The following file within the project was added:**
- WINDOWS/MAKEFILE.NG
- MAKEFILE = MAKEFILE.NG (merge changes from Makefile.vc)
- rename putty.exe to puttyng.exe
- change the "all" target to only build puttyng.exe



For building on Windows:

 - windows/MAKEFILE.NG is for command-line builds on MS Visual C++
   systems. Change into the `windows' subdirectory and type `nmake
   -f MAKEFILE.NG' to build all the PuTTY binaries.

   Last time we checked, PuTTY built with vanilla VC7, or VC6 with
   an up-to-date Platform SDK. (It might still be possible to build
   with vanilla VC6, but you'll certainly have to remove some
   functionality with directives such as NO_IPV6.)


To install for mRemoteNG:

 - Copy the compiled PuTTYNG.exe file to a directory on your root drive. IE: "C:\Program Files (x86)\putty" 
   - You can compile yourself or use the precompiled version in the bin directory.
 - Update the mRemoteNG configuration with the new putty version: Tools > Options > Advanced > Use Custom Putty Path
 - Browse to the location where you copied the new putty binary. IE: "C:\Program Files (x86)\putty\PuTTYNG.exe"  


