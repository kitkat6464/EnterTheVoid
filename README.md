<div align="center">
Cosmic DE Gaming Set Up For EndeavourOS.
</div>
_____________________________________________________________________________________________________________________

## Step 1: Install Cosmic DE With Minimal OOTB Setup With Gaming Stuff: (Run This If You Installed With No Desktop)

```shell
curl -fsSL https://raw.githubusercontent.com/kitkat6464/my_configs/refs/heads/midgard/Installer | sh
```
_____________________________________________________________________________________________________________________

## Step 2: Optimise Your System For Gaming: (RECOMMENDED)

```shell
curl -fsSL https://raw.githubusercontent.com/kitkat6464/my_configs/refs/heads/midgard/Optimise | sh
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
