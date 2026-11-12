---
layout: default
title: Disk
---

## partition
##### **;** _efi 100M_
##### **;** _swap 2-4G_
##### **;** _linux filesystem_
cfdisk

## lvm
pvcreate /dev/$FS   
vgcreate $NAME /dev/$PV   
lvcreate -n $NAME -L $SIZE\_G -l SIZE\_%FREE $VG

## format
mkswap /dev/$SWAP   
mkfs.ext4 /dev/$FS
