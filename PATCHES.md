# GanDesktop patches for gpui-pre-linux 0.3.11

The upstream import commit imports the unmodified crates.io 0.3.11 source archive,
including its published Cargo manifests and Apache-2.0 license. The source
snapshot identifies Zed revision `f816e1f`.

Branch: `gds-0.3.11`.

The patch adds external Wayland/X11 parent identifiers and explicit startup /
activation tokens to the GPUI window API and Linux backend. Platform protocol
objects and dispatch remain inside GPUI.

Apply the `gpui-pre` and `gpui-pre-linux` overrides together. The matching
GanDesktop repositories use the same branch name and retain package version
`0.3.11`, so GPUI Kit's exact version requirements continue to apply.

Changed Rust files:
- `src/linux/wayland/client.rs`
- `src/linux/wayland/window.rs`
- `src/linux/x11/window.rs`

The GDS window-parenting patch is carried forward from `gds-0.3.10`.
