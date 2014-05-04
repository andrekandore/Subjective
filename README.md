
##*SUBJECTIVE*: Windows Port of the Objective-C Runtime

----------------------------------------------------------------------------

**This is a work in progress. Please be *impatient*, contribute!**

----------------------------------------------------------------------------

*SUBJECTIVE* is an attempt to bring Objective C with ARC support to Windows.

This project is a fork of objc4-532.2, the Objective C runtime, available at
opensource.apple.com. It can be compiled using the latest llvm-clang either
on OS X or on Windows. In the former case you will need the MinGW
cross-compiler package for OS X. On both platforms clang is used for compiling
the source, whereas either the MinGW/GNU linker or the MS linker is used for
linking the final binaries.


Current limitations:

• 32-bit only

• No closures/blocks

• No old style GC

• Internals: no vtables, no gdb support, just plain malloc, no
preoptimizations, no "zero-cost try"

Many of these limitations apply to ObjC on 32-bit iOS systems anyway.


Prerequisites:

• MinGW cross-compile environment for OS X:
http://mingw-w64.sourceforge.net/download.php
