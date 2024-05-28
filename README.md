# MBBSEmu Reference Documents

This repository contains all publicly available reference documents which were utilized in the creation of MBBSEmu. These documents include scanned in books, published reference manuals, compiler guides, development guides, portions of SDKs, etc.

## File Descriptions

**84X1440_OS2_Technical_Reference_Volume_2_Sep87.pdf**

Published by IBM in 1987, this OS/2 Reference Manual contains information on the DOSCALLS library implemented by the DOS versions of The MajorBBS and Worldgroup. This manual provides detailed information about these API calls including input, output, and their internal operation.

**210498-005_80286_and_80287_Programmers_Reference_Manual_1987.pdf**

The official 80286/287 Programmers Reference Manual from Intel. Being from Intel, this reference manual is treated as the golden standard for operation of the emulated 16-bit CPU, including details around opcodes and their execution with a 16-bit Environment. 

**230985-003_386DX_Microprocessor_Programmers_Reference_Manual_1990.pdf**

The official 80386DX Microprocessor Programmers Reference Manual from Intel. Again, being this document is from Intel, it is treated as the golden standard for the operation of any emulated 32-bit CPU operations, including details around opcodes and their execution within a 32-bit environment.

Only a couple modules for The MajorBBS/Worldgroup for DOS made use of modern compilers which implemented 32-bit instructions in specific areas. 

**Borland_C++_Version_4.0_Library_Reference_Sep93.pdf**

The Borland C++ Version 4.0 Library Reference manual provides details as to all the run-time functions available through the Borland compiler at that time. This reference manual is used when emulating the function calls that aren't statically linked as part of modules compiled for The MajorBBS/Worldgroup. Because these functions must be emulated, this reference guide is used as the golden standard as to how these functions should operate.

**Btrieve_Programmers_Reference_1998.pdf**

Published by Pervaise Software in 1998, the Btrieve Programmers Reference provides not only programatic details as to the behavior of the Btrieve engine, but also basic information around file and index structure. This manual was helpful in understanding expected return codes from methods for error handling, as well as the multitude of different file options Btrieve databases could be built with. 

**BtrieveStatusCodes.pdf**

Provided by Actian (who purchased Pervasive), this file contains a definition of all the potential Btrieve Status Codes providing a road map of which status codes are required in order to properly convey error scenarios to modules that might be expecting potential non-successful queries.

**development-tips.md**
Internal document from The MajorBBS Emulation Project providing some quick tips on getting your local environment setup for development of MBBSEmu.

**DOS_Interrupts.pdf**
A thorough documentation of all available DOS API calls (Interrupts). Properly being able to emulated DOS Interrupts within MBBSEmu was a critical component to getting EXE emulation working properly. Being there are around a thousand possible APIs, we implement them in the emulator as needed.

**GSBL_Library_Reference_Guide_Rev_N_Jan_1994.pdf**

Official reference guide from Galacticomm published in 1994 from the (at the time) revolutional Galacticomm Software Breakthrough Library. The GSBL is the magic behind The MajorBBS/Worldgroup, allowing it to process multiple channels real time on commodity hardware. The GSBL is responsible for communication to/from the channels as well as some internal controls.

**Intel_Programming_With_The_x87_FPU.pdf**

Reference manual from Intel on programming against the x87 FPU within x86 processors. Emulating the x87 FPU opcodes was required in order to provide support for Floating Point math and the x87 opcodes. This reference guide contains detailed information around the FPU instructions, stack, and inner operation of the FPU during execution.

**Interrupt_Vectors.txt**

A simple list of all known Interrupt Vectors in DOS from both Microsoft, IBM, and other 3rd Party Software. An example being that DOS Extenders would usually occupy INT 0x78, while Novell NetWare would reside on INT 0x6F. This file was helpful to identify the usage of a given Interrupt Vector if it wasn't a standard DOS provided API.

**MajorBBS_Developers_Guide_Rev_6.2_Jan_1994.pdf**

The official MajorBBS Developers Guide 6.2 published in 1994. This guide was intended to accompany the provided SDK to give developers the majority of the information they needed in order to create their own modules. This Developers Guide has detailed information around the provided exported functions which modules would code against. This document provides method signatures, as well as details on the inner operation of the available exported functions. This is the most recent Developer Guide we have been able to locate.

**MBBS_6_2_System_Operations_Guide.zip**

Accompanying the Developers Guide, the System Operations guide was intended to provide Sysops all the information required in order to operate a MajorBBS system. There's not a ton of useful technical information within this guide, but has some nuggets for Sysops looking for help with lesser known parts on the system.

**MSDOS_Encyclopedia_Win16_NE_Header.pdf**

Appendix K from the MSDOS Encyclopedia, this document provides details and structure around the NE (New Executable) file format introduced with Windows 3.0. The modules produced by the MajorBBS SDK and consumed by  The MajorBBS were early DLL files that were compiled into NE format. This document provided us the information we needed to write a file parser to load the NE files, including headers, relation tables, and code/data segments.

**Novell_Btrieve_Installation_and_Operation_Netware51.pdf**

The Official Novell NetWare 5.1 Btrieve Installation and Operation manual. Published in 2000, this manual provides higher level operation and installation of Btrieve. The section of this manual which was very helpful to the development of MBBSEmu was the information around the "BUTIL.EXE" file which is used to generate Btrieve DAT files from a definition file. This manual contained detailed information on those definition files, the properties used, and how to successfully build a Btrieve database.

**PHAPI.h** 

The header file from Phar Lap Software Inc. for the Phar Lap Application Program Interface (PHAPI). The MajorBBS and Worldgroup both used PHAPI on DOS to enable access to extended memory. This interface was extended to modules as well, if they wanted to access extended memory directly.
 
 **PharLap_386DOS_Extender_Reference_Manual.pdf**

 The official Phar Lap 386|DOS-Extender Reference Manual for the SDK of the same name. As with the above header file, this reference manual provides detailed information on the operation of the PHAPI API, allowing us to properly emulate these calls where needed to ensure proper module execution.

**Windows_3.0_16-bit_NE_Executable_Format.txt**

Provides additional details on the 16-bit NE (New Executable) format introduced with Windows 3.0. 

**Worldgroup_312_Developers_Reference.pdf**

This developers reference, provided by Galacticomm, gives some high level information around the SDK and developing Modules for the DOS and Windows versions of Worldgroup 3.12, including supported compilers and environments. 