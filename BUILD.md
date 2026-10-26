# BUILD

Lumen Media Player is built exactly like VLC, because it *is* the VLC tree with packaging
identity replaced. Two build systems are present:

- **Autotools** (`.bootstrap`, `configure`, `make`) — the traditional, best-tested path.
- **Meson** (`meson setup build && ninja -C build`) — the newer path, requires meson >= 1.10.

## Debian / Ubuntu

```sh
sudo apt-get update
sudo apt-get build-dep vlc          # pulls the full dependency set
sudo apt-get install -y build-essential git autopoint gettext libtool automake autoconf pkg-config

./bootstrap                          # regenerate configure (needs autopoint/gettext)
./configure --prefix=/usr/local --enable-qt
make -j$(nproc)
sudo make install
```

## Fedora

```sh
sudo dnf builddep vlc
sudo dnf install -y gcc gcc-c++ make autoconf automake libtool gettext-devel pkgconf-pkg-config
./bootstrap && ./configure --prefix=/usr/local && make -j$(nproc)
```

## macOS

```sh
xcode-select --install
brew install autoconf automake libtool pkg-config gettext meson ninja
export PATH="$(brew --prefix gettext)/bin:$PATH"
./bootstrap && ./configure --prefix=/usr/local && make -j$(sysctl -n hw.ncpu)
```

## Windows

Use the MSYS2/MinGW-w64 environment and `extras/package/win32/build.sh`; the full
procedure lives in `doc/` and on the VLC wiki
(https://wiki.videolan.org/Compile_VLC/). Expect the longest build of the three
platforms because every dependency in `contrib/` is rebuilt from source.

## Meson path

```sh
meson setup build -Dqt=enabled
ninja -C build
sudo ninja -C build install
```

## Notes

- `./configure` is **generated**; it does not exist until `./bootstrap` runs.
- `contrib/` downloads and compiles third-party libraries on first use. Budget
  30-90 minutes the first time on a fast machine, considerably more on Windows.
- Build artefacts go to `build/` (meson) or in-tree (autotools).
- To test without installing, run `./vlc` (autotools) or `./build/bin/vlc` (meson).
- This fork only changed packaging identity; if a build fails, upstream VLC's
  dependency documentation applies unchanged.

## Status of this fork

The rebranding in this archive was produced and integrity-checked on 2026-10-24.
A full compile was **not** completed in the environment that generated it (2 vCPU,
no VLC dependency set installed, no network access to the dependency mirrors) — see
`VERIFICATION.md` for exactly what was and was not run.
