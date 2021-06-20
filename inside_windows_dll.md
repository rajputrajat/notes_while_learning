# PE file format

## Queries:

* Optimization - delay loading of DLLs
* Optimization - section merging
* Optimization - binding
* .NET metadata format
* Thread Local Storage (TLS)
* .rdata storage importance
* PEDUMP program
* VAX/VMS
* COFF
* PE file - debug information section mapping in memory
* RVA (Relative Virtual Addresses)

## Points:

* Portable executable format
* PE files are derived from earlier COFF (Common Object File Format) found on VAX/VMS
* OBJ files emitted bhy Microsoft Compilers use the COFF format
* some fields in COFF, use octal encoding
* 64 bit PE format is called PE32+.
  No new fields were added. One field was deleted.
  Remaining all? widened from 32 to 64 bit.
* Distinction between DLL and EXE files is a single bit. Both use exactly same PE format
* Data structure in a DLL file is same as in memory
* PE files are not just mapped into memory as a single memory-mapped file.
  though the ordering of sections are same, offsets can be different.
* when PE files are loaded in memory by Windows Loader, the in-memory version is known as a module.
  the starting address where the file mapping begins is called an HMODULE.
* PE (as well as COFF) format is described in WINNT.H file.
* "depends" is a program to examine PE files
* To read and modify PE files, Microsoft provides IMAGEHLP.DLL

### PE file sections:

* represents code or data
* data -
    a. read/write program data (global)
    b. API import and export tables
    c. resources
    d. relocations
* each section also contains own set of in-memory attributes:
    a. section contains code
    b. section is rw or ro
    c. data in section is shared between all processes
* section names are solely for the human readability
* names are usually prefixed with 'dot', but that's not a requirement
* you can put your data into a separate section using `#pragma data_seg("my_data")`
* some sections in OBJ files are meant to pass information to LINKER, so these won't make it into the final executable
* PE file specifies 2 type of alignment values - for disk file and the other in memory.
  these values can differ. and each section in PE file start at multiple of these offset values.
  typical value is 0x200.
* Once mapped into memory, sections always start on at least a page boundary.
  each section corresponds to a memory page.
  on x86 - 4KB aligned, on IA-64 - 8KB aligned
* PEDUMP program output of KERNEL32.DLL:
  ```
    Section Table
    01 .text
    VirtSize: 00074658 VirtAddr: 00001000 raw data offs: 00000400 raw data size: 00074800
    02 .data
    VirtSize: 000028CA VirtAddr: 00076000 raw data offs: 00074C00 raw data size: 00002400
  ```
* The .text section is at offset 0x400 in the PE file and will be 0x1000 bytes above
  the load address of KERNEL32 in memory.
  Likewise, the .data section is at file offset 0x74C00 and will be 0x76000 bytes above
  KERNEL32's load address in memory.
* Linker can be asked to merge 2 sections which have compatible attributes, into one.
  this is done via the linker '/merge' switch.
  to combine .text and .rdata => `MERGE:.rdata=.text`
  this can save a 'page' when PE file loaded in memory
* shouldn't merge - .rsrc, .reloc or .pdata into other sections
  prior to .NET .idata could be merged into other sections, but not anymore
  but linker ofter merges parts of .idata into other sections, such as .rdata,
  when doing a relaese build
* Windows Loader writes to portions of 'imports data' when these are loaded, even though these are 
  read-only section. because system can temperarily set the attributes to rw. once initilization is
  done, these are set back to their original attributes

### Relative Virtual Addresses

* RVA = target address - load address (HMODULE)
* call GetModuleHandle with the name of DLL

### The Data Directory

* directory to quickly locate data structures such as imports, exports, resources
  and base relocations
* these are found in consistent manner and the locations is known as the DataDirectory
* is an array of 16 structures
* indexes are IMAGE_DIRECTORY_ENTRY_XXX (0 to 15)

### Importing Functions

* when importing a DLL, Windows Loader locates all the imported functions and data and make those
  available to your code.
* implicit linking and explicit linking
* delayload feature (Visual C++ 6.0) hybrid linking
* In PE file, there's is an array of data structures, one per imported DLL.
  each structure has name of imported DLL and pointer to IAT
* Import Address Table (IAT) - each entry is a pointer to imported function

### PE File Structure

* defined in WINNT.H

#### The MS-DOS header



