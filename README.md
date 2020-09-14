# uss-tools

## ZFS management tools

### bin/zfsman

zfsman will grow (or shrink) an aggregate to be at 70% capacity.

```bash
Ready> bin/zfsman
zfsman v0.1 - Wizard of z/OS 2020

usage: bin/zfsman <dir_name> [-dry]

Will resize a zfs to be at 70% capacity
Options: -dry When using -dry no action will be performed

Ready> bin/zfsman /zdo/rocket
zfsman v0.1

Directory : /zdo/rocket
zFS Aggregate : ZDO.ROCKET.ZFS
Size : 420000
Used/Available : 303440 / 116560
Current Utilization : 73%
Suggested New Size : 433400

Executing : zfsadm grow -aggregate ZDO.ROCKET.ZFS -size 433400

Please stand by...
IOEZ00173I Aggregate ZDO.ROCKET.ZFS successfully grown
ZDO.ROCKET.ZFS (R/W COMP): 130000 K free out of total 433440
Ready>
```

### bin/zfsresize

zfsresize will grow (or shrink) an aggregate to be the desired size

```bash
Ready> bin/zfsman /zdo/rocket
zfsman v0.1

Directory : /zdo/rocket
zFS Aggregate : ZDO.ROCKET.ZFS
Size : 420000
Used/Available : 303440 / 116560
Current Utilization : 73%
Suggested New Size : 433400

Executing : zfsadm grow -aggregate ZDO.ROCKET.ZFS -size 433400

Please stand by...
IOEZ00173I Aggregate ZDO.ROCKET.ZFS successfully grown
ZDO.ROCKET.ZFS (R/W COMP): 130000 K free out of total 433440
Ready>
```

