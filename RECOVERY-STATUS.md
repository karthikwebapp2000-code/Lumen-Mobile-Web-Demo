# Lumen Media Player — Recovery Status

Date: 2026-10-24

## Result

This package is a best-effort recovery from the supplied malformed ZIP. A successful ZIP integrity test on this newly created package means the *new ZIP container* is structurally valid; it does not mean the recovered project is complete, authentic, safe to execute, or buildable.

- Original archive directory: 6,302 entries (5,672 file entries and 630 directory entries).
- Files available through the recovery pass: 3,965.
- Files recovered: 3,957.
- Files that failed decompression or CRC validation: 8.
- Other original file entries could not be recovered from the damaged source archive.
- No build of the full VLC-derived player is claimed or certified.

## Files that failed recovery

- `po/it.po` — invalid stored block lengths
- `po/nb.po` — invalid code lengths
- `po/sl.po` — CRC mismatch
- `po/pa.po` — invalid code lengths
- `modules/demux/g64rtp.c` — invalid distance during decompression
- `modules/video_chroma/copy.c` — CRC mismatch
- `modules/misc/gnutls.c` — invalid distance during decompression
- `modules/gui/macosx/Resources/File-Icons/m4a.icns` — invalid code lengths

## Verification performed on this recovered package

- The newly written ZIP was opened and its CRC test passed for every included entry.
- `COPYING`, `COPYING.LIB`, `AUTHORS`, and `THANKS` were checked against the recovered source tree; this does not independently establish upstream authenticity.
- The `tools/lumen-cli` Python file was syntax-compiled without running it.
- AppStream XML files were checked for XML well-formedness where present.
- The full VLC-derived application was not built or executed.
- This package should not be used as a verified release or distributed as a complete corresponding source archive.

## Recommended next step

Obtain a fresh copy from the project's trusted source and compare a publisher-provided checksum or signature. Re-run the recovery and build checks against that clean source.
