# About this version
This version is specifically for Tucana with mingw for the x86_64-w64-mingw32 and i686-w64-mingw32 toolchains

# cross-sh
A Universal set of scripts to build cross compilers

This builds a linux cross toolchain from scratch for basically and architecture and a variety of C libraries.


# Setup 

## Dependencies
GCC >=8  
Binutils  
GNU Make  
GNU Sed  
wget  
Bash >=5.0  

## Clone this repo
`git clone https://github.com/xXTeraXx/cross-sh-mingw`


## Edit the toolchain.conf 

`nano toolchain.conf` or `vim toolchain.conf`



Set the TARGET_CROSS var to your triplet(eg aarch64-linux-musl)
Set the LIBC var to which one you want (Options between GLIBC, MUSL or newlib)
Finally set the ARCH variable to the one you would need for the kernel compile

Optional: Set the sources dir build dir or the Location of the final cross compiler

Then run the setup.sh script, this will get the sources  
`./setup.sh`

# Build the cross toolchain

`sudo bash build_toolchain.sh`  

# Updating if this gets out of date

Change the versions in toolchain.conf and the URL's in wget to update, as long as the build system hasn't heavily changed, it should work.


