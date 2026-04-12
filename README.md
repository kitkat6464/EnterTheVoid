<div align="center">
ADDING THIS CAUSE INCASE I HIT MY HEAD, AND FORGET HOW TO DO STUFF
</div>

_____________________________________________________________________________________________________________________

> [!IMPORTANT]
> Install Cachy Minimal Or Arch Minimal (No Desktop Option)

_____________________________________________________________________________________________________________________

This Guide Will Help You Setup Niri With Dank Material Shell With Extra Step's For A Stable and Working Out Of The Box Experience. The Step's Begin Below The Screenshot.

_____________________________________________________________________________________________________________________

## Screenshots:

![KitKat's Desktop](assets/kitkat-desktop.png)

*KitKat's Desktop Running Niri With Dank Material Shell*

_____________________________________________________________________________________________________________________

## Step 1: Install Dank Material Shell:

[Dank Shell Installation Guide](https://danklinux.com/docs/getting-started)

_____________________________________________________________________________________________________________________

## Step 2: Install Dank Greeter:

[Dank Greeter Installation Guide](https://danklinux.com/docs/dankgreeter/installation)

NOTE:

PLEASE REBOOT YOUR PC AFTER FOLLOWING THESE 2 STEPS.

_____________________________________________________________________________________________________________________

## Step 3: Setup The Best Out Of The Box Experience:

> [!TIP]
> Install Gaming Packages In The Cachy Hello App If You Are Using CachyOS, This App Will Open After Your First Login.

Before We All Setup The Best Out Of The Box Experience I Will Explain What This Script Installs In The Table's Below.

The Command To Run The Installer Is Beneath These Table's.

| Core Components: | Explanation: |
|:---:|:---:|
|  xdg-desktop-portal-gnome | Backend implementation for xdg-desktop-portal for the GNOME desktop environment
|  gnome-keyring | Stores passwords and encryption keys
|  wlr-randr | Utility to manage outputs of a Wayland compositor
|  cava | Console-based Audio Visualizer with support for multiple backends
|  flatpak | Linux application sandboxing and distribution framework

| Core Applications | Explanation: |
|:---:|:---:|
|  bazaar | A new app store with a focus on flatpaks, particularly Flathub
|  nautilus | Default file manager
|  loupe | A simple image viewer
|  decibels | Audio player
|  showtime | Video player
|  papers | Document viewer for PDF and other document formats
|  gnome-text-editor | A simple text editor
|  lact | Linux GPU Configuration Tool

|  Theming Packages: | Explanation: |
|:---:|:---:|
|  adw-gtk-theme | Unofficial GTK 3 port of the libadwaita theme
|  nwg-look | GTK settings editor adapted to work on wlroots-based compositors
|  qt6ct-kde | Qt 6 Configuration Utility, patched to work correctly with KDE applications

|  Other |
|:---:|
|  Installs mimeapps.list To Your Home's Directory .config Folder To Setup Default Applications |
|  ScopeBuddy To Assist GameScope For Simplicity And Stability |

To Continue, And You Have Read The Table's Above.

Install Using The Command Below In Your Terminal:

```shell
curl -fsSL https://raw.githubusercontent.com/kitkat6464/my_configs/refs/heads/cachydms/InstallPackages | sh
```
_____________________________________________________________________________________________________________________

## Step 4: Setup Secondary Drive Access:

Make a Mounting Folder For The Secondary Drive.

```shell
sudo mkdir /mnt/games
```

Use This Command To Find Your Drive UUID

```shell
lsblk -f
```

Add Your Drive To The fstab File:

```shell
sudo nano /etc/fstab
```
| Example: |
|:---:|
| UUID=YOURDRIVEUUID /mnt/games     btrfs   defaults,noatime,compress=zstd,commit=120 0 0 |

Mount Your New Drive:

```shell
sudo systemctl daemon-reload
```

```shell
sudo mount -a
```
