# dotfilesss
## (WIP) Lobotomized GNOME
![](https://github.com/felipe-juan/dotfilesss/blob/main/ezgif-55b847aaa58db344.gif)


| ![](https://github.com/felipe-juan/dotfilesss/blob/main/Screenshot%20From%202025-11-02%2014-09-36.png)  | ![](https://github.com/felipe-juan/dotfilesss/blob/main/Screenshot%20From%202026-01-18%2015-42-31.png)  | 
| ------------- | ------------- |
| ![](https://github.com/felipe-juan/dotfilesss/blob/main/Screenshot%20From%202025-04-13%2009-26-51.png)  | ![](https://github.com/felipe-juan/dotfilesss/blob/main/Screenshot%20from%202024-10-22%2010-11-36.png)  |

### Current Themes
- Shell: Darkwaita + Custom Orochis Darker and Rosé Pine
  - The first is from the [Darkwaita](https://github.com/varunbpatil/Darkwaita). Just clone his repository in the into `~/.local/share/themes`.
  - I customized both the latter themes to match the Darkwaita's colors. You can download it there. The Rosé Pine is supposed to replace `$HOME/.config/gtk-4.0`, while Orochis to install just like any theme, so `$HOME/.themes/`.
- Icons: WhiteSur / Default 
- Cursor: Bibata Modern Ice
- Dark Pastel - Black Box

### Current Extensions
#### Visuality
- Blur my Shell
- Burn my Windows 
- Compact Top Bar
- Dash to Dock and/or Panel
- Desktop Cube
- Gnome 4x UI Improvements
- Just Perfection
- Rounded Window Corners Reborn
- Search Light
- User Themes

#### Funcionality
- AppIndicator
- Caffeine
- Color Picker
- Media Controls
- Pop Shell / FOrge
- Copyous / Pano Clipboard
- Screen Rotate
- Quick Close in Overview
- Vitals
- RunCat
- Unite

### Current Applications
- Anki
- Bazaar
- Black Box
- Bottles
- Boxes
- Calibre
- Celluloid
- Extension Manager
- Flatseal
- Gear Lever
- Gradia
- Hidamari
- Image viewer
- Inkscape
- IntelliJ Community
- LocalSend
- LibreSprite
- Kasasa
- KDE Connect
- Kdenlive
- KindleComicConverter
- Komikku
- Kooha
- Krita
- Mission Center
- Obsidian
- OBS Studio
- Okular
- OnlyOffice
- Planify
- qBittorrent
- Readest
- Steam
- Stremio
- Syncthing
- Tweaks
- Vesktop
- Video Trimmer
- VSCodium  
- Xournal++
- [YouTube Music](https://github.com/pear-devs/pear-desktop)
- Zen Browser

### Random changes I made recently
- XCompose
  - Despite following the [XCompose instructions](https://github.com/raelgc/win_us_intl) to have a better international keyboard layout, the experience wasn´t smooth since for example, instead `'m`, it ends up being `ḿ`.
  - However, you can edit the XCompose file to reject putting accents even on consoants, as I did. You can download on this repository.
  - And I don´t know if it was supposed to behaviour like this, but I had to copy and paste all the content to be properly recognized as code after extracting it (?) 
- Dash to Panel
  - In order to make it work with the Dash to Dock extension, you have to:
    - Toggle on the "Keep original gnome-shell dash" option.
    - Put it in a different position than the dock (they can't both be on the right side, for example).
    - Toggle off the visibility of the "Taskbar." Personally, I would also toggle off the "Show Applications" button.
- BlackBox
  - 15px Padding
  - Transparency 85%
- Nautilus
  - Install the `ffmpegthumbnailer` package to have thumbnails in all the files as possible.
  - Preferences
    - General
      - Expandable Folders in List View -> ON
    - Perfomance
      - Search in Subfolders -> All Locations
      - Show Thumbnails -> All Files
      - Count Number of Files in Folders -> All Folders
    - Grid View Captions
      - First -> Size
      - Second -> Modified
      - Third -> None 
- Gnome Tweaks
  - Startup Applications
    - Start Syncthing
    - io.github.mrvladus.List
  - Windows
    - Focus on Hover
    - Raise Windows When Focused 
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
  - about:config -> mousewheel.with_control.action -> 5
- Bottles
  - Get sure you installed the flatpak version (.rpm wasn't working)
  - You might put the files in `/home/[your user]/.var/app/com.usebottles.bottles/data/bottles/bottles/[your created bottle]`
- Incoistencies with flatpaks:
  - `sudo flatpak override --filesystem=$HOME/.themes`
  - `sudo flatpak override --filesystem=$HOME/.icons`
  - `sudo flatpak override --filesystem=xdg-config/gtk-3.0`
  - `sudo flatpak override --filesystem=xdg-config/gtk-4.0`
  - `flatpak override --user --filesystem=xdg-config/gtk-4.0`
  - `sudo flatpak override --filesystem=xdg-data/gnome-shell/extensions/unite@hardpixel.eu/styles`
  > Reason: The flatpak versions of these apps still have the top bar, even though it had already been disabled on the Unite extension, and all the other apps had respected that. If it persists, install a non-Flatpak version of the same app.

### GSettings alterations
`gsettings set org.gnome.desktop.wm.preferences mouse-button-modifier '<Alt>'`

`gsettings set org.gnome.desktop.wm.preferences resize-with-right-button true`

`gsettings set org.gnome.shell.window-switcher current-workspace-only false`

`gsettings set org.gnome.shell disable-extension-version-validation true`

`gsettings set org.gnome.desktop.wm.keybindings always-on-top "['<Alt>grave']"` 

`gsettings set org.gnome.desktop.wm.preferences auto-raise-delay 0` 

### /etc/environment edits
```
export GTK_IM_MODULE=cedilla
export QT_IM_MODULE=cedilla
export QT_SCALE_FACTOR=1.1
export QT_QPA_PLATFORMTHEME=‘gnome’
QT_WAYLAND_DISABLE_WINDOWDECORATION=1
GTK_WAYLAND_DISABLE_WINDOWDECORATION=1
```
