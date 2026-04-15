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

## Step 1: Update/Upgrade System Package's:

Make Sure All System Package's Are Up to Date:

```shell
pikman upgrade
```
_____________________________________________________________________________________________________________________

## Step 2: Install/Setup Stock App's:

Install Core Application's:

```shell
pikman install loupe papers gnome-text-editor firefox lact bazaar
```

Setup Default Application's:

```shell
cd $HOME/.config
```

```shell
wget https://raw.githubusercontent.com/kitkat6464/my_configs/refs/heads/pikanoctalia/.config/mimeapps.list
```
_____________________________________________________________________________________________________________________

## Step 1: Setup ScopeBuddy For GameScope:

Install wlr-randr For ScopeBuddy Support On Niri:

```shell
pikman install wlr-randr
```

Install ScopeBuddy:

```shell
sudo curl -Lo /usr/local/bin/scopebuddy https://raw.githubusercontent.com/OpenGamingCollective/ScopeBuddy/refs/tags/1.4.0/bin/scopebuddy
```

```shell
sudo chmod +x /usr/local/bin/scopebuddy
```

```shell
sudo ln -s scopebuddy /usr/local/bin/scb
```
_____________________________________________________________________________________________________________________

## Step 3: Install/Setup Noctalia:

Install Noctalia Shell:

```shell
pikman install noctalia-shell
```

> [!IMPORTANT]
> MAKE SURE TO INSTALL THE NOCTALIA POLKIT PLUGIN BEFORE CONTINUING. Install Noctalia's Polkit From Noctalia's Plugin Page.

Disable Mate's Polkit:

```shell
sudo mv /etc/xdg/autostart/polkit-mate-authentication-agent-1.desktop /etc/xdg/autostart/polkit-mate-authentication-agent-1.desktop.bak
```

_____________________________________________________________________________________________________________________

## Step 2: Setup Secondary Drive Access:

Make a Mounting Folder For The Secondary Drive:

```shell
sudo mkdir /mnt/games
```

Use This Command To Find Your Drive UUID:

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

Reboot Your PC:

```shell
sudo reboot
```

_____________________________________________________________________________________________________________________