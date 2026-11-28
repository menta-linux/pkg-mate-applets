# pkg-mate-applets (Menta Linux)

Debian packaging of mate-applets (Salsa 1.26.1-5) updated to the upstream release
1.28.1 (upstream has no 1.29.0 release). Version: `1.28.1-1menta1`.

Changes: `--enable-in-process` (every applet runs inside mate-panel, required for native
Wayland panels). mate-applets has no Wayland configure switch; its X11-only code
(stickynotes, trash) is guarded by runtime GDK_IS_X11_DISPLAY checks.
Extra patches go in debian/patches (quilt, `series`).

CI builds on push to `master`; tag `menta/<version>` publishes the .debs as a release.
