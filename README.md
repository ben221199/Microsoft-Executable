| Offset | Size | MS-DOS 1.0 (1.25) | MS-DOS 2.0 | MS-DOS 3.0 (3.3) |
| - | - | - | - | - |
| 0x00 | 2 bytes (Word) | `RELPT` | `exe_signature` | `exe_signature` |
| 0x02 | 2 bytes (Word) | `RELSEG` | `exe_len_mod_512` | `exe_len_mod_512` |
| 0x04 | 2 bytes (Word) | `PAGES` | `exe_pages` | `exe_pages` |
| 0x06 | 2 bytes (Word) | `RELCNT` | `exe_rle_count` | `exe_rle_count` |
| 0x08 | 2 bytes (Word) | `HEADSIZ` | `exe_par_dir` | `exe_par_dir` |
| 0x0A | 2 bytes (Word) | ... | `exe_min_BSS` | `exe_min_BSS` |
| 0x0C | 2 bytes (Word) | `LOADLOW` (?) | `exe_max_BSS` | `exe_max_BSS` |
| 0x0E | 2 bytes (Word) | `INITSS` | `exe_SS` | `exe_SS` |
| 0x10 | 2 bytes (Word) | `INITSP` | `exe_SP` | `exe_SP` |
| 0x12 | 2 bytes (Word) | ... | `exe_chksum` | `exe_chksum` |
| 0x14 | 2 bytes (Word) | `INITIP` | `exe_IP` | `exe_IP` |
| 0x16 | 2 bytes (Word) | `INITCS` | `exe_CS` | `exe_CS` |
| 0x18 | 2 bytes (Word) | `RELTAB` | `exe_rle_table` | `exe_rle_table` |
| 0x1A | 2 bytes (Word) | - | `exe_iov` | `exe_iov` |
| 0x1C | 4 bytes (Double Word) | - | `exe_sym_tab` | `exe_sym_tab` |
