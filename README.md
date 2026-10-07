# Custom wlogout Configuration

A personal wlogout customization created while building a minimal Niri-based
Wayland desktop environment on CachyOS.

This project started from an existing wlogout setup and was adapted through
iterative configuration, testing, and visual refinement to fit my workflow
and desktop environment.

## Overview

The configuration provides a minimal, icon-focused power menu with:

- Logout
- Suspend
- Hibernate
- Shutdown
- Reboot
- Custom background
- Custom power icons
- Enlarged icon presentation
- Transparent button styling
- Custom spacing and positioning
- Niri keyboard shortcut integration

The configuration is designed to remain lightweight and easy to modify.

## What I Learned

This project was part of my exploration of the Linux Wayland ecosystem.
Rather than relying entirely on default configurations, I experimented with
the available configuration and styling options and adapted the interface
through repeated testing.

It helped me gain practical experience with:

- Wayland desktop customization
- Niri configuration
- wlogout configuration
- GTK/CSS-based interface styling
- Linux filesystem and configuration management
- Shell-based automation with Fish
- Managing custom assets and relative paths
- Iterative UI refinement and troubleshooting

## Adaptation & Problem Solving

The final configuration was developed through several iterations.

Some of the visual behavior required working within the limitations of
wlogout's supported configuration and CSS properties rather than assuming
that standard web CSS properties would work identically.

The interface was therefore refined by testing different:

- Icon sizes
- Button allocations
- Margins and spacing
- Background positioning
- Hover behavior
- Layout parameters

The final result is intentionally simple while retaining the ability to
adapt the configuration further.

## Project Structure

```text
wlogout-custom/
├── README.md
├── layout
├── style.css
└── icons/
    ├── bg.png
    ├── logout.png
    ├── suspend.png
    ├── hibernate.png
    ├── shutdown.png
    └── reboot.png

#Installation

Copy the configuration into the user wlogout directory:

```fish
mkdir -p ~/.config/wlogout/icons
cp layout ~/.config/wlogout/layout
cp style.css ~/.config/wlogout/style.css
cp icons/*.png ~/.config/wlogout/icons/
```

## Niri Shortcut

For an Alt+F5 power menu shortcut in Niri:

```kdl
Alt+F5 { spawn "wlogout" "-b" "5" "-c" "25" "-r" "0" "-L" "40" "-R" "40" "-T" "380" "-B" "380"; }
```

## wlogout Layout

The menu provides:

- Logout
- Suspend
- Hibernate
- Shutdown
- Reboot

## Requirements

- wlogout
- GTK3
- gtk-layer-shell
- Wayland compositor

Tested with Niri on CachyOS.
