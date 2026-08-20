<div align="center">
Cosmic Desktop Set Up For EndeavourOS.
</div>
_____________________________________________________________________________________________________________________

## Step 1: Install Cosmic Desktop With Minimal Set Of Apps: (Run This If You Installed With No Desktop)

```shell
curl -fsSL https://raw.githubusercontent.com/kitkat6464/EnterTheVoid/refs/heads/cosmic/01-Desktop | sh
```
_____________________________________________________________________________________________________________________

## Step 2: Install Gaming Essential Like Steam, GameScope, ScopeBuddy, and MangoHud: (Install if You Want Gaming)

```shell
curl -fsSL https://raw.githubusercontent.com/kitkat6464/EnterTheVoid/refs/heads/cosmic/02-Gaming | sh
```
_____________________________________________________________________________________________________________________

## Step 3: Optimise Your System For Gaming: (RECOMMENDED)

```shell
curl -fsSL https://raw.githubusercontent.com/kitkat6464/EnterTheVoid/refs/heads/cosmic/03-Optimise | sh
```
_____________________________________________________________________________________________________________________

## Step 4: Setup VM Host Tools (Optional)

```shell
curl -fsSL https://raw.githubusercontent.com/kitkat6464/EnterTheVoid/refs/heads/cosmic/04-VM | sh
```
_____________________________________________________________________________________________________________________

## Step 5: Setup Secondary Drive:

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
