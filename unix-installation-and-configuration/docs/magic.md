# The file command and magic

All Dyalog APL binary files have a unique magic number: the first byte is always 0xAA (decimal 170), and the second identifies the type of Dyalog file. Additional bytes may in some cases be used to further identify the type, version and state of the file. UNIX systems include the `file` command which use the information in the magic file to describe the contents of files.

## magic and AIX

AIX still uses a very early version of `magic`, so it is not possible to give as much information about Dyalog APL files as on Linux.

Dyalog provides a file, `magic`, which is located in the top level installation directory of Dyalog APL. To use this file to extend the capabilities of the `file` command either run
```apl
file -m /opt/mdyalog//32/classic/p5/magic *
```

or catenate the contents of /opt/mdyalog//32/classic/p5/magic onto /etc/magic, and then run
```apl
file *
```

## Example:
```apl
$ file -m /opt/mdyalog//32/classic/p6/magic *
1_apl_j1: Dyalog APL component file 64-bit level 1 journaled non-checksummed
1_apl_j2: Dyalog APL component file 64-bit level 2 journaled checksummed
1_apl_qfile: Dyalog APL component file 64-bit non-journaled non-checksummed
1_big1: Dyalog APL component file 64-bit level 2 journaled checksummed
1_big2: Dyalog APL component file 64-bit level 1 journaled checksummed
apl64u: Dyalog APL workspace type 12 subtype 4 64-bit unicode big-endian
aplout: Dyalog APL workspace type 12 subtype 0 32-bit classic little-endian
aplcore: Dyalog APL workspace type 12 subtype 4 32-bit classic little-endian
colours: Dyalog APL workspace type 12 subtype 4 32-bit classic little-endian
core: data or International Language text
signals: Dyalog APL workspace type 12 subtype 4 32-bit classic little-endian
utf8: Dyalog APL workspace type 12 subtype 4 32-bit unicode little-endian
```

### magic and Linux

Most Linux distributions include details about Dyalog-related files in their magic files; Dyalog has submitted two versions of the magic file for inclusion in distributions. To check whether your Linux distribution has the more recent version, create a journaled component file and then run the file command against that component file. The two examples below show the output with the earlier and later versions of magic in use.

## Example, using the older default magic file:
```apl
$ file *
1_apl_j1: data
1_apl_j2: data
1_apl_qfile: data
1_big1: data
1_big2: data
apl64u: \012- Dyalog APL\012- workspace\012- version 12\012- .4
aplout: \012- Dyalog APL\012- workspace\012- version 12\012- .0
aplcore: \012- Dyalog APL\012- workspace\012- version 12\012- .4
colours: \012- Dyalog APL\012- workspace\012- version 12\012- .4
core: ELF 32-bit LSB core file Intel 80386, version 1 (SYSV), SVR4-style
signals: \012- Dyalog APL\012- workspace\012- version 12\012- .4
utf8: \012- Dyalog APL\012- workspace\012- version 12\012- .4

```

## Example, with more recent magic file:
```apl

$ file *
1_apl_j1: Dyalog APL component file 64-bit level 1 journaled non-checksummed
1_apl_j2: Dyalog APL component file 64-bit level 2 journaled checksummed
1_apl_qfile: Dyalog APL component file 64-bit non-journaled non-checksummed
1_big1: Dyalog APL component file 64-bit level 2 journaled checksummed
1_big2: Dyalog APL component file 64-bit level 1 journaled checksummed
apl64u: Dyalog APL workspace type 12 subtype 4 64-bit unicode big-endian
aplout: Dyalog APL workspace type 12 subtype 0 32-bit classic little-endian
aplcore: Dyalog APL workspace type 12 subtype 4 32-bit classic little-endian
colours: Dyalog APL workspace type 12 subtype 4 32-bit classic little-endian
core: ELF 32-bit LSB core file Intel 80386, version 1 (SYSV), SVR4-style, from '/opt/mdyalog/14.0/32/classic/dyalog'
signals: Dyalog APL workspace type 12 subtype 4 32-bit classic little-endian
utf8: Dyalog APL workspace type 12 subtype 4 32-bit unicode little-endian
```

The most recent version of the magic file can be found in the top level of the installation directory; see the man page for the file command for details of how to update the system magic file, or use the syntax described in the /etc/magic and AIX section above to override the default magic file with the one supplied in the installation directory.
