<div align="center">
ADDING THIS CAUSE INCASE I HIT MY HEAD, AND FORGET HOW TO DO STUFF
</div>
_____________________________________________________________________________________________________________________

<div align="center">
My Dot Files Are In The config Branch. Keeping 2 Branches Separated To Keep Thing's Clean And Organised.

[You Can Find Them Here](https://github.com/kitkat6464/my_configs/tree/configs)

</div>

> [!IMPORTANT]
> Install Using The PikaOS's Niri ISO.

## Screenshots:

![KitKat's Desktop](kitkats-desktop.png)

*KitKat's Desktop Included With Desktop Widget's Running Niri/Noctalia Shell On PikaOS*
_____________________________________________________________________________________________________________________

## Step 1: Update/Upgrade System Package's:

```shell
pikman upgrade
```
_____________________________________________________________________________________________________________________

## Step 2: Install/Setup Stock App's:

```shell
pikman install loupe papers gnome-text-editor secrets firefox lact bazaar fastfetch
```
_____________________________________________________________________________________________________________________

## Step 3: Setup Default Application's:

```shell
cd $HOME/.config
```

```shell
wget https://raw.githubusercontent.com/kitkat6464/my_configs/refs/heads/configs/.config/mimeapps.list
```
_____________________________________________________________________________________________________________________

## Step 3: Install wlr-randr For ScopeBuddy:

```shell
pikman install wlr-randr
```
_____________________________________________________________________________________________________________________

## Step 3: Install ScopeBuddy:

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

## Step 4: Install/Setup Noctalia:

```shell
pikman install noctalia-shell
```

> [!IMPORTANT]
> MAKE SURE TO INSTALL THE NOCTALIA POLKIT PLUGIN BEFORE CONTINUING. Install Noctalia's Polkit From Noctalia's Plugin Page. This Command Will Disable Mate's Polkit

```shell
sudo mv /etc/xdg/autostart/polkit-mate-authentication-agent-1.desktop /etc/xdg/autostart/polkit-mate-authentication-agent-1.desktop.bak
```
_____________________________________________________________________________________________________________________

## Step 5: Install And Fix Font's:

```shell
pikman install fonts-noto fonts-noto-color-emoji
```

```shell
fc-cache -f
```
_____________________________________________________________________________________________________________________

## Step 6: Setup Secondary Drive Access:

```shell
sudo mkdir /mnt/games
```

> [!IMPORTANT]
> Use This Command To Find Your Drive UUID.

```shell
lsblk -f
```

> [!IMPORTANT]
> Modify fstab Very Carefully.

```shell
sudo nano /etc/fstab
```

| Example: |
|:---:|
| UUID=YOURDRIVEUUID /mnt/games     btrfs   defaults,noatime,x-gvfs-show,compress=zstd,commit=120 0 0 |

> [!IMPORTANT]
> Now Reboot Your PC.

```shell
sudo reboot
```
_____________________________________________________________________________________________________________________
