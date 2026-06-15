# NDC - Niri Display Configurator

NDC (Niri Display Configurator) is a premium, visual display arrangement utility designed specifically for the **Niri** scrollable-tiling Wayland compositor on CachyOS (or any other distribution running Niri).

It opens as a floating popup window showing a visual layout of your current display configuration, allowing you to drag-and-drop, scale, rotate, enable, and align monitors with pixel-perfect snapping.

---

## Features

- **Visual Layout Editor**: Displays a scaled visual representation of your connected monitors on a grid canvas.
- **Drag & Drop Arrangement**: Easily move your monitors by dragging them with your mouse.
- **Magnetic Snapping**: Automatically snaps screen edges and corners together when close for flawless alignment. 
- **Shift to Bypass Snapping**: Hold down the **Shift** key while dragging to disable snapping for free-form placement.
- **Coordinate Inputs**: Configure positions manually with `X` and `Y` logical coordinate fields with real-time bidirectional syncing.
- **Full Display Parameter Control**:
  - **Resolution & Refresh Rate**: Select from a dropdown populated with all available video modes queried dynamically from the compositor.
  - **Scale Factor**: Fine-tune custom scaling factors (e.g., `1.0`, `1.25`, `1.50`, etc.).
  - **Transform (Rotation)**: Select rotation options (`normal`, `90`, `180`, `270`, etc.) and watch the canvas aspect ratio update in real-time.
  - **Toggle Enabled State**: Easily toggle monitors on/off (translates to the Niri `off` directive).
- **10-Second Safety Confirmation**: When applying a new layout, the configurator triggers a countdown safety check. If you don't confirm the new settings within 10 seconds (or if you close the window/press **Esc**), the configuration instantly rolls back to your last confirmed setup.
- **Premium Styling**: Dark-mode aesthetic, glowing active states, responsive grid scaling, and custom styling.

---

## Installation

Run the install script from the project root to install the binary to `~/.local/bin/ndc` and register it with your Niri keybindings (`Mod+P`):

```bash
chmod +x install
./install
```

## Uninstallation

To completely remove NDC, revert all modifications to your Niri configuration files, and delete the local binaries, run the uninstall script:

```bash
chmod +x uninstall
./uninstall
```

## Shortcuts

- **Esc**: Instantly close the window (performs auto-revert if in confirmation countdown mode).
- **Shift (hold)**: Temporarily disables edge snapping during drag-and-drop.
