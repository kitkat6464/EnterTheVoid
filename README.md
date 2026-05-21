<div align="center">
Needing Access To A Bleeding Edge Traditional Distro ATM. Dev Packages Too Out Dated On PikaOS.
</div>
_____________________________________________________________________________________________________________________

## Step 1: Install OOTB Experience:

```shell
curl -fsSL https://raw.githubusercontent.com/kitkat6464/my_configs/refs/heads/midgard/Installer | sh
```
_____________________________________________________________________________________________________________________

## Step 2: Setup Secondary Drive Access:

```shell
sudo mkdir /mnt/games
```

> [!IMPORTANT]
> Use This Command To Find The Drive's UUID.

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
> Now Reboot PC.

```shell
sudo reboot
```
_____________________________________________________________________________________________________________________
