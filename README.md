<div align="center">
Mango With Noctalia Set Up For EndeavourOS.
</div>

> [!IMPORTANT]
> READ INSTALLER FILE TO SEE WHAT GETS INSTALLED. Fork This Repo and Remove Stuff You Don't Need Or If You Want To Add Something.


_____________________________________________________________________________________________________________________

## Step 0: Install Mango From The AUR (Run This If You Installed With No Desktop)

```shell
yay -S mangowm
```

_____________________________________________________________________________________________________________________

## Step 1: Install Noctalia Along With Useful Apps:

```shell
curl -fsSL https://raw.githubusercontent.com/kitkat6464/MyConfigs/refs/heads/mango/Required-Setup | sh
```

_____________________________________________________________________________________________________________________

## Step 2: Setup VM Host Tools (OPTIONAL)

```shell
curl -fsSL https://raw.githubusercontent.com/kitkat6464/MyConfigs/refs/heads/mango/Optional-VM | sh
```
_____________________________________________________________________________________________________________________

## Step 3: Setup Secondary Drive:

```shell
sudo mkdir /mnt/games
```

> [!IMPORTANT]
> Use This Command To Find The Drive's UUID.

```shell
lsblk -f
```

> [!IMPORTANT]
> Modify fstab Carefully.

```shell
sudo nano /etc/fstab
```

| Example: |
|:---:|
| UUID=YOURDRIVEUUID /mnt/games     btrfs   defaults,noatime,x-gvfs-show,compress=zstd,commit=120 0 0 |

> [!IMPORTANT]
> Now Reboot PC.

```shell
sudo reboot
```
_____________________________________________________________________________________________________________________
