---
title: "MATLABオンラインVMスペック"
linkTitle: "MATLABonlineVM"
date: 2022-02-25
categories: "Development"
pickups: ["MATLAB"]
tags:
- MATLAB online
- VM
- MATLAB
- Simulink
description: >
  MATLAB onlineのVMインスタンススペックを確認しておく
marp: true
theme: slide_style
size: 16:9
paginate: true
headingDivider: 2
header: "[社内資料] MATLAB online"
footer: (C)2022 PUES Corp.
---
# <!-- fit --> :memo: MATLABオンラインVMスペック
<!-- _class: title -->

![bg blur:5px](2022-03-16-10-47-43.png)

## プロセッサ

:computer: 15コアの様子

```
processer: 15
vendor_id: GenuineIntel
cpu family: 6
model: 85
model name: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.5GHz
stepping: 7
microcode: 0x500320a
cpu MHz: 3070.332
chache size: 36608 KB
```

## メモリ

```
>> system('cat /proc/meminfo')
MemTotal:       130517732 kB
MemFree:        13271368 kB
MemAvailable:   26916768 kB
Buffers:         1818028 kB
Cached:         12002796 kB
SwapCached:            0 kB
Active:         108286024 kB
Inactive:        5985008 kB
Active(anon):   100452748 kB
Inactive(anon):    41320 kB
Active(file):    7833276 kB
Inactive(file):  5943688 kB
Unevictable:           0 kB
Mlocked:               0 kB
SwapTotal:             0 kB
SwapFree:              0 kB
Dirty:              3252 kB
Writeback:          4272 kB
AnonPages:      100449700 kB
Mapped:          1529484 kB
Shmem:             44152 kB
Slab:            1804276 kB
SReclaimable:    1102532 kB
SUnreclaim:       701744 kB
KernelStack:      280192 kB
PageTables:       506212 kB
NFS_Unstable:          0 kB
Bounce:                0 kB
WritebackTmp:          0 kB
CommitLimit:    65258864 kB
Committed_AS:   174894228 kB
VmallocTotal:   34359738367 kB
VmallocUsed:           0 kB
VmallocChunk:          0 kB
HardwareCorrupted:     0 kB
AnonHugePages:         0 kB
ShmemHugePages:        0 kB
ShmemPmdMapped:        0 kB
CmaTotal:              0 kB
CmaFree:               0 kB
HugePages_Total:       0
HugePages_Free:        0
HugePages_Rsvd:        0
HugePages_Surp:        0
Hugepagesize:       2048 kB
DirectMap4k:      282532 kB
DirectMap2M:    43276288 kB
DirectMap1G:    89128960 kB
```

## OS

```
>> system('cat /etc/issue')
Ubuntu 18.04.4 LTS \n \l
```
