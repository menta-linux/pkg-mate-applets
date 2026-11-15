# pkg-mate-applets (Menta Linux)

Debian packaging of mate-applets (Salsa 1.26.1-5) updated to an upstream git snapshot:
upstream has no 1.29.0 tag/release; master `e4b07e6` (2026-10-20) is v1.28.1+22 commits
(its configure.ac still says 1.28.1). Version: `1.28.1+git20261020.e4b07e6-1menta1`.

Changes: `--enable-in-process` (every applet runs inside mate-panel, required for native
Wayland panels), new build-deps libsoup-3.0 / json-glib. mate-applets has no Wayland
configure switch; its X11-only code (stickynotes, trash) is guarded by runtime
GDK_IS_X11_DISPLAY checks.

CI builds on push to `master`; tag `menta/<version>` publishes the .debs as a release.
