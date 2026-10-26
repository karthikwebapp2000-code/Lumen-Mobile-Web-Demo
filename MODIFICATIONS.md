# MODIFICATIONS

Fork of VLC media player → Lumen Media Player
Date: 2026-10-24
Based on: VLC 4.0.0-dev (`AC_INIT([vlc], [4.0.0-dev])`, upstream codename "Otto Chriek")

This file is the GPLv2 §2a modification notice for this fork.

## Packaging identity

- `configure.ac`: `AC_INIT([vlc], ...)` → `AC_INIT([lumen], ...)`; codename
  "Otto Chriek" → "First Light".
- `meson.build`: `project('VLC', ...)` → `project('Lumen', ...)`; codename updated.
- Desktop entries renamed and rewritten: `vlc.desktop.in` → `lumen.desktop.in`,
  and the four `vlc-open*.desktop.in` handler entries.
- AppStream metadata: `org.videolan.vlc.appdata.xml.in.in` →
  `org.lumen.lumen.appdata.xml.in.in`.
- `share/Info.plist.in` (macOS bundle identity) and `share/Makefile.am`
  references updated to the renamed assets.

## Artwork

- Full icon set regenerated (16/24/32/48/64/128/256/512 px + `.ico`): a teal-to-navy
  rounded square with a white play triangle.
- The VideoLAN cone logo is removed from all bundled artwork; no VLC icon file
  remains in `share/icons/`.

## Documentation

- `README.md` rewritten for the fork, with attribution and GPL obligations.
- Upstream `README.md` preserved verbatim as `README.upstream.md`.
- Added `NOTICE.md`, `BUILD.md`, `MODIFICATIONS.md`, `VERIFICATION.md`.

## Unmodified

- Every copyright header in every source file.
- `COPYING`, `COPYING.LIB`, `AUTHORS`, `THANKS`, `ABOUT-NLS` — byte-identical to
  upstream (md5 compared).
- All C / C++ / Obj-C / Rust source code and all `po/` translations.
