<div align="center">
ADDING THIS CAUSE INCASE I HIT MY HEAD, AND FORGET HOW TO DO STUFF
</div>

> [!TIP]
> Install Using Cachy Minimal or Arch Minimal (No Desktop Option)

## Screenshots

![KitKat's Desktop](assets/kitkat-desktop.png)
*KitKat's running with Niri and Dank Material Shell*

## Step 1: Install Dank Shell Using That Beautiful TTY:

[Dank Shell Installation Guide](https://danklinux.com/docs/getting-started)

## Step 2: Install Dank Greeter Cause That's Hot AF:

[Dank Greeter Installation Guide](https://danklinux.com/docs/dankgreeter/installation)

REBOOT YOUR PC AFTER FOLLOWING THESE 2 STEPS.

> [!TIP]
> Install Gaming Packages in Cachy Hello app, the app will open after first login, if you are using CachyOS

## Step 3: Install Missing Stuff:
(This Adds Missing Stuff Like File Manager, Photo Viewer, Video Player, Music Player, Missing Deps For Consistency, and Gamescope Tiling Support)

```shell
curl -fsSL https://raw.githubusercontent.com/kitkat6464/my_configs/refs/heads/cachyos/AfterInstall | sh
```

## Step 4: Install's Lact and QT Theming Support From The AUR:

```shell
curl -fsSL https://raw.githubusercontent.com/kitkat6464/my_configs/refs/heads/cachyos/AfterInstallAur | sh
```

## Step 5: Setup File Extension Support:

```shell
cd .config
```

```shell
wget https://raw.githubusercontent.com/kitkat6464/my_configs/refs/heads/cachyos/.config/mimeapps.list
```

## Step 6: Setup Secondary Drive Access:

Make Mounting Folder For Secondary Drive.

```shell
sudo mkdir /mnt/games
```

> [!TIP]
> Using This Command In The Terminal Will Find Your Drive UUID -> lsblk -f

Add Drive To fstab File:

```shell
sudo nano /etc/fstab
```

> UUID=YOURDRIVEUUID /mnt/games     btrfs   defaults,noatime,compress=zstd,commit=120 0 0

Mount Your New Drive:

```shell
sudo systemctl daemon-reload
```

```shell
sudo mount -a
```

## Step 7: Install ScopeBuddy: (This Is To Make Games Work Nicely)

> [!TIP]
> For more info about ScopeBuddy, visit https://docs.bazzite.gg/Advanced/scopebuddy/

Using curl:
```shell
sudo curl -Lo /usr/local/bin/scopebuddy https://raw.githubusercontent.com/HikariKnight/ScopeBuddy/refs/tags/1.3.0/bin/scopebuddy
```

```shell
sudo chmod +x /usr/local/bin/scopebuddy
```

Make scb symlink because we love short commands
```shell
sudo ln -s scopebuddy /usr/local/bin/scb
```
