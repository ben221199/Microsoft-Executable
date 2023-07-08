| Offset | Size | MS-DOS 1.0 (1.25)<sup>[1]</sup><br><sub>and MS-DOS 2.0<sup>[2] [3]</sup></sub> | MS-DOS 2.0<sup>[4] [5]</sup><br><sub>and MS-DOS 3.0 (3.3)<sup>[6]</sup></sub> | Description |
| - | - | - | - | - |
| 0x00 | 2 bytes (Word) | `RELPT` | `exe_signature` | Signature |
| 0x02 | 2 bytes (Word) | `RELSEG` | `exe_len_mod_512` | Length of last page |
| 0x04 | 2 bytes (Word) | `PAGES` | `exe_pages` | Amount of pages |
| 0x06 | 2 bytes (Word) | `RELCNT` | `exe_rle_count` | Relocation count |
| 0x08 | 2 bytes (Word) | `HEADSIZ` | `exe_par_dir` | Header size in paragraphs |
| 0x0A | 2 bytes (Word) | ... | `exe_min_BSS` | Minimum number of paragraphs of BSS (?) |
| 0x0C | 2 bytes (Word) | `LOADLOW` (?) | `exe_max_BSS` | Maximum number of paragraphs of BSS (?) |
| 0x0E | 2 bytes (Word) | `INITSS` | `exe_SS` | Initial SS value |
| 0x10 | 2 bytes (Word) | `INITSP` | `exe_SP` | Initial SP value |
| 0x12 | 2 bytes (Word) | ... | `exe_chksum` | Checksum |
| 0x14 | 2 bytes (Word) | `INITIP` | `exe_IP` | Initial IP value |
| 0x16 | 2 bytes (Word) | `INITCS` | `exe_CS` | Initial CS value |
| 0x18 | 2 bytes (Word) | `RELTAB` | `exe_rle_table` | Relocation table address |
| 0x1A | 2 bytes (Word) | ❌ | `exe_iov` | (Index)? Overlay number |
| 0x1C | 4 bytes (Double Word) | ❌ | `exe_sym_tab` | Symbol table address |

[1]: https://github.com/microsoft/MS-DOS/blob/master/v1.25/source/COMMAND.ASM
[2]: https://github.com/microsoft/MS-DOS/blob/master/v2.0/source/EXE2BIN.ASM
[3]: https://github.com/microsoft/MS-DOS/blob/master/v2.0/source/PROFIL.ASM

[4]: https://github.com/microsoft/MS-DOS/blob/master/v2.0/source/DOSSYM.ASM
[5]: https://github.com/microsoft/MS-DOS/blob/master/v2.0/source/DOSSYM_v211.ASM
[6]: https://github.com/AR1972/DOS3.3/blob/master/SRC/DOS/EXE.INC
