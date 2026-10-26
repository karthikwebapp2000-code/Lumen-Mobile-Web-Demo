# Lumen Media Player

**Lumen Media Player** is a libre and open source media player and multimedia engine,
focused on **playing everything**, and **running everywhere**.

Lumen can play most multimedia files, discs, streams and devices, and can also
convert, encode, stream and manipulate streams into numerous formats.

The engine of Lumen is embeddable in 3rd party applications and is called
*liblumen*.

Lumen is a **fork of the VLC media player**, created by the
[VideoLAN project](https://videolan.org) and developed by a community of volunteers.
The original project started at the university
[École Centrale Paris](https://www.centralesupelec.fr/), which relicensed VLC under
GPLv2 in February 2001. Since then VLC has been downloaded billions of times.

> ## Attribution
>
> This software is **based on VLC**, Copyright © the VideoLAN team and the VLC authors.
> It is **not** an official VideoLAN release, is **not** endorsed by or affiliated with
> VideoLAN, and must not be presented as "VLC". The original authors are credited in
> [`AUTHORS`](AUTHORS), [`THANKS`](THANKS) and [`NOTICE.md`](NOTICE.md), and the
> upstream README is preserved verbatim as [`README.upstream.md`](README.upstream.md).
> The "VLC" name and the cone logo are VideoLAN trademarks and are **not** used here.

## Archive recovery status

**Important:** This folder was recovered from a malformed ZIP archive, not from a fresh, independently verified upstream checkout. The original archive listed 6,302 entries (5,672 file entries), while the recovery process could access 3,965 file entries; 3,957 files were recovered and 8 additional files failed decompression or CRC validation. Other original entries could not be recovered from the damaged archive. Therefore this is a best-effort recovery, **not a complete or build-verified source release**.

See [`RECOVERY-STATUS.md`](RECOVERY-STATUS.md) for the exact files that failed recovery. Obtain a fresh trusted source archive before attempting a production build or distributing binaries.

## License

Lumen is released under the **GPLv2 (or later)** license, inherited from VLC.
On some platforms it is de facto GPLv3, because of the licenses of dependencies.

`liblumen`, the engine, is released under the **LGPLv2 (or later)** license. This allows
embedding the engine in 3rd party applications while letting them be licensed under other
terms.

Full license texts, unmodified, are in this repository:

- [`COPYING`](COPYING) — GNU General Public License v2
- [`COPYING.LIB`](COPYING.LIB) — GNU Lesser General Public License v2.1

### Obligations when you distribute a build

- Publish the **complete corresponding source code** for every binary you ship,
  including your modifications, under the same GPLv2 (or later) terms.
- **Mark modified files** with a prominent notice stating the change and its date
  (GPLv2 §2a) — see [`MODIFICATIONS.md`](MODIFICATIONS.md).
- Keep copyright notices, the license texts and the no-warranty disclaimer intact
  and pass them to everyone who receives a copy.
- Do not relicense VLC-derived code, and add no restrictions on top of the GPL.
  Your own original branding, artwork and separately written code may carry your
  own license — the code you received may not.

## Building

See [`BUILD.md`](BUILD.md). Short version on Debian/Ubuntu:

```sh
./bootstrap
./configure --prefix=/usr/local
make -j$(nproc)
sudo make install
```

First run fetches and builds third-party dependencies from `contrib/`, which takes a
long time (tens of minutes on a fast machine, much longer on Windows/macOS).

## Changes in this fork

See [`MODIFICATIONS.md`](MODIFICATIONS.md). Fork date: 2026-10-24.

## Links

- Fork repository — https://example.org/lumen/lumen
- Upstream VLC — https://www.videolan.org/vlc/
- Upstream support — https://www.videolan.org/support/
- Upstream wiki — https://wiki.videolan.org/
- VLC hacking guide — https://wiki.videolan.org/Hacker_Guide
