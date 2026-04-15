<div align="center">
ADDING THIS CAUSE INCASE I HIT MY HEAD, AND FORGET HOW TO DO STUFF
</div>

_____________________________________________________________________________________________________________________

> [!IMPORTANT]
> Install Using The PikaOS's Niri ISO.

_____________________________________________________________________________________________________________________

## Screenshots:

![KitKat's Desktop](kitkat-desktop.png)

*KitKat's Desktop Running Niri/Noctalia Shell On PikaOS*

_____________________________________________________________________________________________________________________

## Step 1: Setup The Best Out Of The Box Experience:

Before We All Setup The Best Out Of The Box Experience I Will Explain What This Script Installs In The Table's Below.

The Command To Run The Installer Is Beneath These Table's.

| Applications | Explanation: |
|:---:|:---:|
|  loupe |
|  gnome-music |
|  papers |
|  gnome-text-editor |

| Tool's | Explanation: |
|:---:|:---:|
|  firefox |
|  bazaar |
|  lact |

To Continue, And You Have Read The Table's Above.

Install Using The Command Below In Your Terminal:

```shell
curl -fsSL https://raw.githubusercontent.com/kitkat6464/my_configs/refs/heads/pikanoctalia/InstallPackages | sh
```
_____________________________________________________________________________________________________________________

## Step 2: Setup Secondary Drive Access:

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
| UUID=YOURDRIVEUUID /mnt/games     btrfs   defaults,noatime,x-gvfs-show,compress=zstd,commit=120 0 0 |

Reboot:

```shell
sudo reboot
```