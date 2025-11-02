# dotfilesss
## (WIP) A simpler Linux rice.
![](https://github.com/felipe-juan/dotfilesss/blob/main/Screenshot%20From%202025-11-02%2013-50-40.png)
![](https://github.com/felipe-juan/dotfilesss/blob/main/Screenshot%20from%202024-10-22%2010-11-36.png)
![](https://github.com/felipe-juan/dotfilesss/blob/main/Screenshot%20From%202025-11-02%2014-09-36.png)

### Current Themes
- Orochis Dark / High Contrast Inverse
- WhiteSur Icons / Default Icons
- Default Fonts
- Bibata Modern Ice
- Dark Pastel - Black Box

### Current Extensions
#### Visuality
- Blur my Shell
- Dash to Dock
- Dash to Panel / Compact Top Bar
- Desktop Cube
- Gnome 4x UI Improvements
- Hanabi Extension
- Just Perfection
- Search Light
- Unite

#### Funcionality
- AppIndicator
- Caffeine
- Color Picker
- Media Controls
- Pano - Clipboard Manager
- Pop Shell
- Screen Rotate
- Quick Close in Overview
- RunCat / Vitals

### Current Applications
- Anki
- Black Box
- Bottles
- Calibre
- Cozy
- Drawing
- Extension Manager
- Foliarte
- Frog
- Gear Lever
- Gradia
- Imgae Viewer (native)
- Inkscape
- IntelliJ Community
- LocalSend
- LibreSprite
- Kasasa
- KDE Connect
- Kdenlive
- KindleComicConverter
- Komikku
- Krita
- Obsidian
- OBS Studio
- OnlyOffice
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
- Vesktop
- Video Player (native)
- Video Trimmer
- Virtual Machine Manager
- VSCodium
- Xournal++
- [YouTube Music](https://github.com/pear-devs/pear-desktop)
- Zen Browser

### Random changes I made recently
- Dash to Panel
  - In order to make it work with the Dash to Dock extension, you have to:
    - Toggle on the "Keep original gnome-shell dash" option.
    - Put it in a different position than the dock (they can't both be on the right side, for example).
    - Toggle off the visibility of the "Taskbar." Personally, I would also toggle off the "Show Applications" button.
- BlackBox
  - No transparency
  - 15px Padding
- Gnome Tweaks
  - Startup Applications
    - Start Syncthing
    - io.github.mrvladus.List
  - Windows
    - Focus on Hover 
- Pop Shell
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
- Incoistencies with flatpaks:
  - `sudo flatpak override --filesystem=xdg-config/gtk-3.0`
  - `sudo flatpak override --filesystem=xdg-config/gtk-4.0`
  - `sudo flatpak override --filesystem=xdg-data/gnome-shell/extensions/unite@hardpixel.eu/styles`
  > Reason: the flatpak versions of these apps would still have the top bar even though  had already been disabled on the Unite extension and all the other apps had respected it. If despite that it persists, so install a non-flatpak version of the same app.

### GSettings alterations
`gsettings set org.gnome.desktop.wm.preferences mouse-button-modifier '<Alt>'`

`gsettings set org.gnome.desktop.wm.preferences resize-with-right-button true`

`gsettings set org.gnome.shell.window-switcher current-workspace-only false`

`gsettings set org.gnome.shell disable-extension-version-validation true`

### /etc/environment edits
```
export GTK_IM_MODULE=cedilla
export QT_IM_MODULE=cedilla
QT_WAYLAND_DISABLE_WINDOWDECORATION=1
GTK_WAYLAND_DISABLE_WINDOWDECORATION=1
```
