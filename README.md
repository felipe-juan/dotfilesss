# dotfilesss
## (WIP) A simpler Linux rice.
![](https://github.com/felipe-juan/dotfilesss/blob/main/Screenshot%20from%202024-10-22%2010-11-36.png)
![](https://github.com/felipe-juan/dotfilesss/blob/main/Screenshot%20From%202025-04-13%2010-53-18.png)

### Current Themes
- Orochis Dark / High Contrast Inverse
- WhiteSur Icons / Default Icons
- Default Fonts
- Bibata Modern Ice
- Dark Pastel - Black Box

### Current Extensions
#### Visuality
- Blur my Shell
- Compact Top Bar
- Desktop Cube
- Gnome 4x UI Improvements
- Hanabi Extension
- Just Perfection
- Rounded Window Corners Reborn
- Unite

#### Funcionality
- AppIndicator
- Color Picker
- Dash to Dock
- Media Controls
- Pano - Clipboard Manager
- Pop Shell
- Quick Close in Overview
- Vitals

### Current Applications
- Anki
- Black Box
- Bottles
- Calibre
- Celluloid
- Cozy
- DaVinci Resolve
- Drawing
- Extension Manager
- Foliarte
- Frog
- Gear Lever
- Gradia
- Image Viewer
- Inkscape
- IntelliJ Community
- LocalSend
- LibreSprite
- Kasasa
- KindleComicConverter
- Krita
- Obsidian
- OBS Studio
- OneDrive + GUI
- OpenTabletDriver
- Steam
- YouTube Music
- qBittorrent
- Papers
- Refine
- Stremio
- Syncthing
- Todoist
- Tweaks
- Video Trimmer
- VSCodium
- Xournal++
- Zen Browser

### Random changes I made recently
- BlackBox
  - No transparency
  - 15px Padding
- Gnome Tweaks
  - Startup Applications
    - Start Syncthing
    - io.github.mrvladus.List
  - Windows
    - Focus on Hover 
- Pop Shell / Forge
  - White Outline
  - Smart Gaps Disabled (Pop Shell)
- Settings / Tweaks
  - Display > 100% Scale
  - Font: 1.20 Scaling
  > Fractional Scaling still sucks on Linux. So since I use a 14" laptop, the larger font makes for it.
- OpenTabletDriver
  - DualActionBinds Plugin
  - Pen Binding: `E:B`
- ZenBrowser / FireFox
  - about:config -> disable middle click paste
- Bottles
  - Get sure you installed the flatpak version (.rpm wasn't working)
  - You might put the files in `/home/[your user]/.var/app/com.usebottles.bottles/data/bottles/bottles/[your created bottle]`
- Install non-flatpak version of following apps (rpm / appimage):
  - Blender
  - LibreSprite
  - Xournal++
  - OpenTabletDriver
  > Reason: the flatpak versions of these apps still had the top bar, even though it had already been disabled and all the other apps had respected it.

### GSettings alterations
`gsettings set org.gnome.desktop.wm.preferences mouse-button-modifier '<Alt>'`

`gsettings set org.gnome.desktop.wm.preferences resize-with-right-button true`

`gsettings set org.gnome.shell.window-switcher current-workspace-only false`

### /etc/environment edits
```
export GTK_IM_MODULE=cedilla
export QT_IM_MODULE=cedilla
QT_WAYLAND_DISABLE_WINDOWDECORATION=1
GTK_WAYLAND_DISABLE_WINDOWDECORATION=1
```
