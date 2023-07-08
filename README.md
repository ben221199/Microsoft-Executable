| Offset | Size | Initial version | Extended version | New version | Description |
| - | - | - | - | - | - |
| Name | N/A | `RUNVAR` | `EXE_file` | `IMAGE_DOS_HEADER` (name not seen in SDK) | Name of the struct |
| Version | N/A | MS-DOS 1.0 (1.25)<sup>[1]</sup><br>MS-DOS 2.0<sup>[2] [3]</sup> | MS-DOS 2.0<sup>[4] [5]</sup><br>MS-DOS 3.0 (3.3)<sup>[6]</sup> | Windows 1.0 (and later) | Used in OS version |
| 0x00 | 2 bytes (Word) | `RELPT` | `exe_signature` | `e_magic` | Signature |
| 0x02 | 2 bytes (Word) | `RELSEG` | `exe_len_mod_512` | `e_cblp` | Length of last page |
| 0x04 | 2 bytes (Word) | `PAGES` | `exe_pages` | `e_cp` | Amount of pages |
| 0x06 | 2 bytes (Word) | `RELCNT` | `exe_rle_count` | `e_crlc` | Relocation count |
| 0x08 | 2 bytes (Word) | `HEADSIZ` | `exe_par_dir` | `e_cparhdr` | Header size in paragraphs |
| 0x0A | 2 bytes (Word) | ... | `exe_min_BSS` | `e_minalloc` | Minimum number of paragraphs of BSS (?) |
| 0x0C | 2 bytes (Word) | `LOADLOW` (?) | `exe_max_BSS` | `e_maxalloc` | Maximum number of paragraphs of BSS (?) |
| 0x0E | 2 bytes (Word) | `INITSS` | `exe_SS` | `e_ss` | Initial SS value |
| 0x10 | 2 bytes (Word) | `INITSP` | `exe_SP` | `e_sp` | Initial SP value |
| 0x12 | 2 bytes (Word) | ... | `exe_chksum` | `e_csum` | Checksum |
| 0x14 | 2 bytes (Word) | `INITIP` | `exe_IP` | `e_ip` | Initial IP value |
| 0x16 | 2 bytes (Word) | `INITCS` | `exe_CS` | `e_cs` | Initial CS value |
| 0x18 | 2 bytes (Word) | `RELTAB` | `exe_rle_table` | `e_lfarlc` | Relocation table address |
| 0x1A | 2 bytes (Word) | ❌ | `exe_iov` | `e_ovno` | (Index)? Overlay number |
| 0x1C | 4 bytes (Double Word) | ❌ | `exe_sym_tab` | `e_res1` | Symbol table address |
| 0x20 | 4 bytes (Double Word) | ❌ | ❌ | remaining of `e_res1` | Reserved |
| 0x24 | 2 bytes (Word) | ❌ | ❌ | `e_oemid` | OEM ID |
| 0x26 | 2 bytes (Word) | ❌ | ❌ | `e_oeminfo` | OEM Information |
| 0x28 | 20 bytes | ❌ | ❌ | `e_res2` | Reserved |
| 0x3C | 4 bytes (Double Word) | ❌ | ❌ | `e_lfanew` | New executable address |

[1]: https://github.com/microsoft/MS-DOS/blob/master/v1.25/source/COMMAND.ASM
[2]: https://github.com/microsoft/MS-DOS/blob/master/v2.0/source/EXE2BIN.ASM
[3]: https://github.com/microsoft/MS-DOS/blob/master/v2.0/source/PROFIL.ASM

[4]: https://github.com/microsoft/MS-DOS/blob/master/v2.0/source/DOSSYM.ASM
[5]: https://github.com/microsoft/MS-DOS/blob/master/v2.0/source/DOSSYM_v211.ASM
[6]: https://github.com/AR1972/DOS3.3/blob/master/SRC/DOS/EXE.INC
