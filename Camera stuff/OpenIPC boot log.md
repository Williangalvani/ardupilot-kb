                         


System startup

Uncompress Ok!

U-Boot 2016.11 (Sep 15 2023 - 12:52:59 +0800)hi3516av300

Relocation Offset is: 0f6c0000
Relocating to 8fec0000, new gd at 8fe1fef0, sp at 8fe1fed0
SPI Nor:  hifmc_ip_ver_check(44): Check Flash Memory Controller v100 ...hifmc_ip_ver_check(50):  Found
hifmc_spi_nor_probe(1664): SPI Nor ID Table Version 1.0
hifmc_spi_nor_probe(1689): SPI Nor(cs 0) ID: 0xc2 0x20 0x18
hifmc_spi_nor_probe(1754): Block:64KB hifmc_spi_nor_probe(1755): Chip:16MB hifmc_spi_nor_probe(1756): Name:"MX25L128XX"
hifmc100_spi_nor_probe(147): SPI Nor total size: 16MB
NAND:  0 MiB
MMC:   
In:    serial
Out:   serial
Err:   serial
Net:   eth0
Warning: eth0 (eth0) using random MAC address - 62:49:99:8a:03:73

Hit any key to stop autoboot:  2  1  0 
device 0 offset 0x100000, size 0x200000

SF: 2097152 bytes @ 0x100000 Read: OK
## Booting kernel from Legacy Image at 82000000 ...
   Image Name:   Linux-4.9.37-hi3516av300
   Image Type:   ARM Linux Kernel Image (uncompressed)
   Data Size:    2030169 Bytes = 1.9 MiB
   Load Address: 80008000
   Entry Point:  80008000
   Loading Kernel Image ... OK

Starting kernel ...

Booting Linux on physical CPU 0x0
Linux version 4.9.37 (runner@fv-az993-378) (buildroot-gcc-12.2.0) #1 SMP Thu Sep 14 11:34:18 UTC 2023
CPU: ARMv7 Processor [410fc075] revision 5 (ARMv7), cr=10c5387d
CPU: div instructions available: patching division code
CPU: PIPT / VIPT nonaliasing data cache, VIPT aliasing instruction cache
OF: fdt:Machine model: Hisilicon HI3516DV300 DEMO Board
cma zone is not set!
cma: Reserved 16 MiB at 0x9f000000
Memory policy: Data cache writealloc
percpu: Embedded 13 pages/cpu @debca000 s21644 r8192 d23412 u53248
Built 1 zonelists in Zone order, mobility grouping on.  Total pages: 130048
Kernel command line: mem=512M console=ttyAMA0,115200 root=/dev/mtdblock2 rootfstype=squashfs init=/init mtdparts=hi_sfc:1M(boot),2M(kernel),10M(rootfs),-(rootfs_data)
PID hash table entries: 2048 (order: 1, 8192 bytes)
Dentry cache hash table entries: 65536 (order: 6, 262144 bytes)
Inode-cache hash table entries: 32768 (order: 5, 131072 bytes)
Memory: 495560K/524288K available (4096K kernel code, 162K rwdata, 940K rodata, 1024K init, 272K bss, 12344K reserved, 16384K cma-reserved, 0K highmem)
Virtual kernel memory layout:
    vector  : 0xffff0000 - 0xffff1000   (   4 kB)
    fixmap  : 0xffc00000 - 0xfff00000   (3072 kB)
    vmalloc : 0xe0800000 - 0xff800000   ( 496 MB)
    lowmem  : 0xc0000000 - 0xe0000000   ( 512 MB)
    pkmap   : 0xbfe00000 - 0xc0000000   (   2 MB)
    modules : 0xbf000000 - 0xbfe00000   (  14 MB)
      .text : 0xc0008000 - 0xc0500000   (5088 kB)
      .init : 0xc0700000 - 0xc0800000   (1024 kB)
      .data : 0xc0800000 - 0xc0828b00   ( 163 kB)
       .bss : 0xc082a000 - 0xc086e19c   ( 273 kB)
SLUB: HWalign=64, Order=0-3, MinObjects=0, CPUs=2, Nodes=1
Hierarchical RCU implementation.
	Build-time adjustment of leaf fanout to 32.
NR_IRQS:16 nr_irqs:16 16
Gic dist init...
arm_arch_timer: Architected cp15 timer(s) running at 50.00MHz (phys).
clocksource: arch_sys_counter: mask: 0xffffffffffffff max_cycles: 0xb8812736b, max_idle_ns: 440795202655 ns
sched_clock: 56 bits at 50MHz, resolution 20ns, wraps every 4398046511100ns
Switching to timer-based delay loop, resolution 20ns
clocksource: hisp804: mask: 0xffffffff max_cycles: 0xffffffff, max_idle_ns: 637086815595 ns
Console: colour dummy device 80x30
Calibrating delay loop (skipped), value calculated using timer frequency.. 100.00 BogoMIPS (lpj=500000)
pid_max: default: 32768 minimum: 301
Mount-cache hash table entries: 1024 (order: 0, 4096 bytes)
Mountpoint-cache hash table entries: 1024 (order: 0, 4096 bytes)
CPU: Testing write buffer coherency: ok
CPU0: thread -1, cpu 0, socket 0, mpidr 80000000
Setting up static identity map for 0x80100000 - 0x80100058
CPU1: thread -1, cpu 1, socket 0, mpidr 80000001
Brought up 2 CPUs
SMP: Total of 2 processors activated (200.00 BogoMIPS).
CPU: All CPU(s) started in SVC mode.
devtmpfs: initialized
VFP support v0.3: implementor 41 architecture 2 part 30 variant 7 rev 5
clocksource: jiffies: mask: 0xffffffff max_cycles: 0xffffffff, max_idle_ns: 19112604462750000 ns
futex hash table entries: 512 (order: 3, 32768 bytes)
pinctrl core: initialized pinctrl subsystem
NET: Registered protocol family 16
DMA: preallocated 256 KiB pool for atomic coherent allocations
Serial: AMBA PL011 UART driver
120a0000.uart: ttyAMA0 at MMIO 0x120a0000 (irq = 21, base_baud = 0) is a PL011 rev2
console [ttyAMA0] enabled
SCSI subsystem initialized
ssp-pl022 120c0000.spi: ARM PL022 driver, device ID: 0x00800022
ssp-pl022 120c0000.spi: mapped registers from 0x120c0000 to e0834000
ssp-pl022 120c1000.spi: ARM PL022 driver, device ID: 0x00800022
ssp-pl022 120c1000.spi: mapped registers from 0x120c1000 to e0838000
ssp-pl022 120c2000.spi: ARM PL022 driver, device ID: 0x00800022
ssp-pl022 120c2000.spi: mapped registers from 0x120c2000 to e083a000
usbcore: registered new interface driver usbfs
usbcore: registered new interface driver hub
usbcore: registered new device driver usb
clocksource: Switched to clocksource hisp804
NET: Registered protocol family 2
TCP established hash table entries: 4096 (order: 2, 16384 bytes)
TCP bind hash table entries: 4096 (order: 3, 32768 bytes)
TCP: Hash tables configured (established 4096 bind 4096)
UDP hash table entries: 256 (order: 1, 8192 bytes)
UDP-Lite hash table entries: 256 (order: 1, 8192 bytes)
NET: Registered protocol family 1
RPC: Registered named UNIX socket transport module.
RPC: Registered udp transport module.
RPC: Registered tcp transport module.
RPC: Registered tcp NFSv4.1 backchannel transport module.
workingset: timestamp_bits=30 max_order=17 bucket_order=0
squashfs: version 4.0 (2009/01/31) Phillip Lougher
NFS: Registering the id_resolver key type
Key type id_resolver registered
Key type id_legacy registered
jffs2: version 2.2 (NAND) (ZLIB) (RTIME) (c) 2001-2006 Red Hat, Inc.
Block layer SCSI generic (bsg) driver version 0.4 loaded (major 252)
io scheduler noop registered
io scheduler deadline registered (default)
pl061_gpio 120d0000.gpio_chip: PL061 GPIO chip @0x120d0000 registered
pl061_gpio 120d1000.gpio_chip: PL061 GPIO chip @0x120d1000 registered
pl061_gpio 120d2000.gpio_chip: PL061 GPIO chip @0x120d2000 registered
pl061_gpio 120d3000.gpio_chip: PL061 GPIO chip @0x120d3000 registered
pl061_gpio 120d4000.gpio_chip: PL061 GPIO chip @0x120d4000 registered
pl061_gpio 120d5000.gpio_chip: PL061 GPIO chip @0x120d5000 registered
pl061_gpio 120d6000.gpio_chip: PL061 GPIO chip @0x120d6000 registered
pl061_gpio 120d7000.gpio_chip: PL061 GPIO chip @0x120d7000 registered
pl061_gpio 120d8000.gpio_chip: PL061 GPIO chip @0x120d8000 registered
pl061_gpio 120d9000.gpio_chip: PL061 GPIO chip @0x120d9000 registered
pl061_gpio 120da000.gpio_chip: PL061 GPIO chip @0x120da000 registered
pl061_gpio 120db000.gpio_chip: PL061 GPIO chip @0x120db000 registered
brd: module loaded
loop: module loaded
hisi-sfc hisi_spi_nor.0: SPI Nor ID Table Version 1.2
hisi-sfc hisi_spi_nor.0: all blocks is unlocked.
hisi-sfc hisi_spi_nor.0: mx25l12835f (Chipsize 16 Mbytes, Blocksize 64KiB)
4 cmdlinepart partitions found on MTD device hi_sfc
4 cmdlinepart partitions found on MTD device hi_sfc
Creating 4 MTD partitions on "hi_sfc":
0x000000000000-0x000000100000 : "boot"
0x000000100000-0x000000300000 : "kernel"
0x000000300000-0x000000d00000 : "rootfs"
0x000000d00000-0x000001000000 : "rootfs_data"
SPI Nand ID Table Version 2.7
Cannot found a valid SPI Nand Device
hisi_spi_nand_probe(175): Error: driver probe, result: -19
libphy: hisi_femac_mii_bus: probed
libphy: Fixed MDIO Bus: probed
Generic PHY 10011100.mdio:01: attached PHY driver [Generic PHY] (mii_bus:phy_addr=10011100.mdio:01, irq=-1)
phy_id=0x937c4024, phy_mode=rmii
hisi-femac 10010000.ethernet: using random MAC address 02:b1:58:34:20:88
xhci-hcd 100e0000.xhci_0: xHCI Host Controller
xhci-hcd 100e0000.xhci_0: new USB bus registered, assigned bus number 1
xhci-hcd 100e0000.xhci_0: hcc params 0x0220fe6c hci version 0x110 quirks 0x20010010
xhci-hcd 100e0000.xhci_0: irq 28, io mem 0x100e0000
hub 1-0:1.0: USB hub found
hub 1-0:1.0: 1 port detected
xhci-hcd 100e0000.xhci_0: xHCI Host Controller
xhci-hcd 100e0000.xhci_0: new USB bus registered, assigned bus number 2
usb usb2: We don't know the algorithms for LPM for this host, disabling LPM.
hub 2-0:1.0: USB hub found
hub 2-0:1.0: hub can't support USB3.0
usbcore: registered new interface driver usb-storage
hibvt_rtc 12080000.rtc: rtc core: registered 12080000.rtc as rtc0
hibvt_rtc 12080000.rtc: RTC driver for hibvt enabled
i2c /dev entries driver
hibvt-i2c 120b0000.i2c: hibvt-i2c0@100000hz registered
hibvt-i2c 120b1000.i2c: hibvt-i2c1@100000hz registered
hibvt-i2c 120b2000.i2c: hibvt-i2c2@100000hz registered
hibvt-i2c 120b3000.i2c: hibvt-i2c3@100000hz registered
hibvt-i2c 120b4000.i2c: hibvt-i2c4@100000hz registered
hibvt-i2c 120b5000.i2c: hibvt-i2c5@100000hz registered
hibvt-i2c 120b6000.i2c: hibvt-i2c6@100000hz registered
hibvt-i2c 120b7000.i2c: hibvt-i2c7@100000hz registered
himci: mmc host probe
NET: Registered protocol family 10
NET: Registered protocol family 17
Key type dns_resolver registered
Registering SWP/SWPB emulation handler
hibvt_rtc 12080000.rtc: setting system clock to 1970-01-01 00:00:05 UTC (5)
VFS: Mounted root (squashfs filesystem) readonly on device 31:2.
devtmpfs: mounted
Freeing unused kernel memory: 1024K (c0700000 - c0800000)
jffs2: notice: (647) jffs2_build_xattr_subsystem: complete building xattr subsystem, 0 of xdatum (0 unchecked, 0 orphan) and 0 of xref (0 dead, 0 orphan) found.
Timezone env variable not found, using system default.
Thu Sep 14 11:37:55 GMT 2023
Starting syslogd: OK
Starting klogd: OK
Running sysctl: OK
Loading modules:modprobe: module exfat not found in modules.dep
Seeding 2048 bits without crediting
Saving 2048 bits of non-creditable seed for next boot
Starting rngd: GPIO not set. Exiting
OK
Starting mdev...
Starting network: udhcpc: started, v1.36.0
udhcpc: broadcasting discover
udhcpc: broadcasting discover
udhcpc: broadcasting discover
udhcpc: broadcasting discover
udhcpc: broadcasting discover
udhcpc: broadcasting select for 192.168.15.8, server 192.168.15.1
udhcpc: lease of 192.168.15.8 obtained from 192.168.15.1, lease time 14400
deleting routers
adding dns 192.168.15.1
OK
Starting ntpd: OK
Starting dropbear sshd: OK
Production mode
Starting httpd: OK
Starting mini-snmpd: DISABLED, OK
Starting telnetd: DISABLED, OK
Starting crond: OK

Loading of kernel modules...
mmz_start: 0x82000000, mmz_size: 32M
hisilicon: Get data from environment and set SENSOR as unknown
Starting motiondetection.sh: OK
Starting telegram-bot.sh: OK
hisilicon: Loading video system has started...
Starting majestic: OK
Starting rc.local

Welcome to OpenIPC

openipc-hi3516av300 login: 