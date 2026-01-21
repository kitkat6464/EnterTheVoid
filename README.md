<div align="center">
ADDING THIS CAUSE INCASE I HIT MY HEAD, AND FORGET HOW TO DO STUFF
</div>

> [!TIP]
> Install Cachy Minimal Or Arch Minimal (No Desktop Option)

## Screenshots:

![KitKat's Desktop](assets/kitkat-desktop.png)

*KitKat's Desktop Running Niri With Dank Material Shell*

## Step 1: Install Dank Material Shell:

[Dank Shell Installation Guide](https://danklinux.com/docs/getting-started)

## Step 2: Install Dank Greeter:

[Dank Greeter Installation Guide](https://danklinux.com/docs/dankgreeter/installation)

REBOOT YOUR PC AFTER FOLLOWING THESE 2 STEPS.

> [!TIP]
> Install Gaming Packages In The Cachy Hello App If You Are Using CachyOS, This App Will Open After Your First Login.

## Step 3: Install Recommended Packages, Setup Default Apps, And Install ScopeBuddy For GameScope:

**Core Components:**
- xdg-desktop-portal-gnome
- gnome-keyring
- wlr-randr
- cava
- flatpak

**Core Applications:**
- bazaar (App Store)
- nautilus (File Manager)
- loupe (Image Viewer)
- decibels (Audio Player)
- showtime (Video Player)
- papers (Document Viewer)
- gnome-text-editor (Text Editor)
- lact (GPU Utility)
- gpu-screen-recorder-gtk (Screen Recorder)

**Theming Packages:**
- adw-gtk-theme
- nwg-look
- qt6ct-kde

**Other:**
- Installs mimeapps.list to .config To Setup Defaulty Applications
- ScopeBuddy To Assist GameScope For Simplicity

Run The Installer.

```shell
curl -fsSL https://raw.githubusercontent.com/kitkat6464/my_configs/refs/heads/cachyos/InstallPackages | sh
```

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

Example: UUID=YOURDRIVEUUID /mnt/games     btrfs   defaults,noatime,compress=zstd,commit=120 0 0

Mount Your New Drive:

```shell
sudo systemctl daemon-reload
```

```shell
sudo mount -a
```
