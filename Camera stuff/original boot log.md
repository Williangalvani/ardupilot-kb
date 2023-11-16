
```
System startup
  
Uncompress Ok!
  
U-Boot 2016.11 (Nov 25 2022 - 14:30:34 +0800)hi3516av300
  
Relocation Offset is: 0f6d1000
Relocating to 8fed1000, new gd at 8fe90ef0, sp at 8fe90ed0
SPI Nor: hifmc_ip_ver_check(54): Check Flash Memory Controller v100 ...hifmc_ip_ver_check(60): Found
hifmc_spi_nor_probe(2070): SPI Nor ID Table Version 1.0
hifmc_spi_nor_probe(2095): SPI Nor(cs 0) ID: 0xc2 0x20 0x18
hifmc_init_print(2016): Block:64KB hifmc_init_print(2017): Chip:16MB hifmc_init_print(2018): Name:"MX25L128XX"
hifmc100_spi_nor_probe(145): SPI Nor total size: 16MB
NAND: 0 MiB
MMC:
In: serial
Out: serial
Err: serial
Net: eth0
bootshell = 0
device 0 offset 0x80000, size 0x280000
  
SF: 2621440 bytes @ 0x80000 Read: OK
## Booting kernel from Legacy Image at 82000000 ...
Image Name: Linux-4.9.37
Image Type: ARM Linux Kernel Image (uncompressed)
Data Size: 2364417 Bytes = 2.3 MiB
Load Address: 80008000
Entry Point: 80008000
Loading Kernel Image ... OK
  
Starting kernel ...
  
Booting Linux on physical CPU 0x0
Linux version 4.9.37 (cb@hiface) (gcc version 6.3.0 (HC&C V1R3C00SPC200B005_20190606) ) #2 SMP Mon Oct 10 15:09:00 CST 2022
CPU: ARMv7 Processor [410fc075] revision 5 (ARMv7), cr=10c5387d
CPU: div instructions available: patching division code
CPU: PIPT / VIPT nonaliasing data cache, VIPT aliasing instruction cache
OF: fdt:Machine model: Hisilicon HI3516DV300 DEMO Board
cma zone is not set!
cma: Reserved 16 MiB at 0xa7000000
Memory policy: Data cache writealloc
percpu: Embedded 12 pages/cpu @e6acb000 s17676 r8192 d23284 u49152
Built 1 zonelists in Zone order, mobility grouping on. Total pages: 162560
Kernel command line: mem=640M console=ttyAMA0,115200 root=/dev/mtdblock2 rootfstype=squashfs rootfstype=squashfs mtdparts=hi_sfc:512k(boot),2560k(kernel),5M(rootfs),7680K(appfs),512K(fconfigs)
PID hash table entries: 4096 (order: 2, 16384 bytes)
Dentry cache hash table entries: 131072 (order: 7, 524288 bytes)
Inode-cache hash table entries: 65536 (order: 6, 262144 bytes)
Memory: 624160K/655360K available (5120K kernel code, 158K rwdata, 1164K rodata, 1024K init, 314K bss, 14816K reserved, 16384K cma-reserved, 0K highmem)
Virtual kernel memory layout:
vector : 0xffff0000 - 0xffff1000 ( 4 kB)
fixmap : 0xffc00000 - 0xfff00000 (3072 kB)
vmalloc : 0xe8800000 - 0xff800000 ( 368 MB)
lowmem : 0xc0000000 - 0xe8000000 ( 640 MB)
pkmap : 0xbfe00000 - 0xc0000000 ( 2 MB)
modules : 0xbf000000 - 0xbfe00000 ( 14 MB)
.text : 0xc0008000 - 0xc0600000 (6112 kB)
.init : 0xc0800000 - 0xc0900000 (1024 kB)
.data : 0xc0900000 - 0xc09278c0 ( 159 kB)
.bss : 0xc0929000 - 0xc09778ec ( 315 kB)
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
Mount-cache hash table entries: 2048 (order: 1, 8192 bytes)
Mountpoint-cache hash table entries: 2048 (order: 1, 8192 bytes)
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
120a1000.uart: ttyAMA1 at MMIO 0x120a1000 (irq = 22, base_baud = 0) is a PL011 rev2
120a2000.uart: ttyAMA2 at MMIO 0x120a2000 (irq = 23, base_baud = 0) is a PL011 rev2
120a3000.uart: ttyAMA3 at MMIO 0x120a3000 (irq = 24, base_baud = 0) is a PL011 rev2
120a4000.uart: ttyAMA4 at MMIO 0x120a4000 (irq = 25, base_baud = 0) is a PL011 rev2
ssp-pl022 120c0000.spi: ARM PL022 driver, device ID: 0x00800022
ssp-pl022 120c0000.spi: mapped registers from 0x120c0000 to e8844000
ssp-pl022 120c1000.spi: ARM PL022 driver, device ID: 0x00800022
ssp-pl022 120c1000.spi: mapped registers from 0x120c1000 to e8848000
ssp-pl022 120c2000.spi: ARM PL022 driver, device ID: 0x00800022
ssp-pl022 120c2000.spi: mapped registers from 0x120c2000 to e884a000
usbcore: registered new interface driver usbfs
usbcore: registered new interface driver hub
usbcore: registered new device driver usb
clocksource: Switched to clocksource hisp804
NET: Registered protocol family 2
TCP established hash table entries: 8192 (order: 3, 32768 bytes)
TCP bind hash table entries: 8192 (order: 4, 65536 bytes)
TCP: Hash tables configured (established 8192 bind 8192)
UDP hash table entries: 512 (order: 2, 16384 bytes)
UDP-Lite hash table entries: 512 (order: 2, 16384 bytes)
NET: Registered protocol family 1
RPC: Registered named UNIX socket transport module.
RPC: Registered udp transport module.
RPC: Registered tcp transport module.
RPC: Registered tcp NFSv4.1 backchannel transport module.
workingset: timestamp_bits=30 max_order=18 bucket_order=0
squashfs: version 4.0 (2009/01/31) Phillip Lougher
NFS: Registering the id_resolver key type
Key type id_resolver registered
Key type id_legacy registered
jffs2: version 2.2 (NAND) (ZLIB) (RTIME) (c) 2001-2006 Red Hat, Inc.
fuse init (API version 7.26)
Block layer SCSI generic (bsg) driver version 0.4 loaded (major 252)
io scheduler noop registered
io scheduler deadline registered
io scheduler cfq registered (default)
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
hisi-sfc hisi_spi_nor.0: SPI Nor ID Table Version 1.2
hisi-sfc hisi_spi_nor.0: all blocks is unlocked.
hisi-sfc hisi_spi_nor.0: mx25l12835f (Chipsize 16 Mbytes, Blocksize 64KiB)
5 cmdlinepart partitions found on MTD device hi_sfc
5 cmdlinepart partitions found on MTD device hi_sfc
Creating 5 MTD partitions on "hi_sfc":
0x000000000000-0x000000080000 : "boot"
0x000000080000-0x000000300000 : "kernel"
0x000000300000-0x000000800000 : "rootfs"
0x000000800000-0x000000f80000 : "appfs"
0x000000f80000-0x000001000000 : "fconfigs"
SPI Nand ID Table Version 2.7
Cannot found a valid SPI Nand Device
hisi_spi_nand_probe(175): Error: driver probe, result: -19
libphy: hisi_femac_mii_bus: probed
libphy: Fixed MDIO Bus: probed
Generic PHY 10011100.mdio:01: attached PHY driver [Generic PHY] (mii_bus:phy_addr=10011100.mdio:01, irq=-1)
phy_id=0x937c4024, phy_mode=rmii
hisi-femac 10010000.ethernet: using random MAC address 96:88:d3:84:a2:3e
usbcore: registered new interface driver r8152
usbcore: registered new interface driver asix
usbcore: registered new interface driver ax88179_178a
usbcore: registered new interface driver cdc_ether
usbcore: registered new interface driver net1080
usbcore: registered new interface driver rndis_host
usbcore: registered new interface driver cdc_subset
usbcore: registered new interface driver zaurus
usbcore: registered new interface driver cdc_ncm
xhci-hcd 100e0000.xhci_0: xHCI Host Controller
xhci-hcd 100e0000.xhci_0: new USB bus registered, assigned bus number 1
xhci-hcd 100e0000.xhci_0: hcc params 0x0220fe6c hci version 0x110 quirks 0x20010010
xhci-hcd 100e0000.xhci_0: irq 31, io mem 0x100e0000
hub 1-0:1.0: USB hub found
hub 1-0:1.0: 1 port detected
xhci-hcd 100e0000.xhci_0: xHCI Host Controller
xhci-hcd 100e0000.xhci_0: new USB bus registered, assigned bus number 2
usb usb2: We don't know the algorithms for LPM for this host, disabling LPM.
hub 2-0:1.0: USB hub found
hub 2-0:1.0: hub can't support USB3.0
usbcore: registered new interface driver cdc_acm
cdc_acm: USB Abstract Control Model driver for USB modems and ISDN adapters
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
8021q: 802.1Q VLAN Support v1.8
Key type dns_resolver registered
Registering SWP/SWPB emulation handler
hibvt_rtc 12080000.rtc: setting system clock to 2023-08-23 17:48:56 UTC (1692812936)
squashfs: SQUASHFS error: Xattrs in filesystem, these will be ignored
squashfs: SQUASHFS error: unable to read xattr id index table
VFS: Mounted root (squashfs filesystem) readonly on device 31:2.
devtmpfs: mounted
Freeing unused kernel memory: 1024K (c0800000 - c0900000)
  
_ _ _ _ _ _ _ _ _ _ _ _
\ _ _ _ _ _ ___
/ /__/ \ |_/
/ __ / - _ ___
/ / / / / /
_ _ _ _/ / / \_/ \_ ______
___________\___\__________________
  
[RCS]: /etc/init.d/S00devs
mknod: /dev/console: File exists
mknod: /dev/ttyAMA0: File exists
mknod: /dev/ttyAMA1: File exists
mknod: /dev/null: File exists
[RCS]: /etc/init.d/S01udev
random: udevd: uninitialized urandom read (16 bytes read)
udevd[84]: starting eudev-3.2.7
[RCS]: /etc/init.d/S80network
@@@@update main ReadParam ok
IPv6: ADDRCONF(NETDEV_UP): eth0: link is not ready
start task
http accept.....
chmod: /appfs/fconfigs/other/telnet_open: No such file or directory
RTC date/time: 23/8/2023 17:48:57
Get RTC Successful
MSG_Init.....
sdap start, port[32872]
[planB.c,232] bc:07:18:01:20:4c
[planB.c,239] ip: 192.168.2.10
[planB.c,266] waiting...
[M_SysLog_Read_Cfg 175] not exits log file
umount: can't unmount /opt/ddrlog/syslog/: No such file or directory
HiFace Main software 3.021.3.3_MAIN_V36(230711) compile time is Jul 11 2023 18:54:01
ENCRYPT_FLASH_ReadConfig nLen = 1060
ENCRYPT_CONFIG_INFO_S=1060
chpasswd: password for 'root' changed
hisi-femac 10010000.ethernet eth0: Link is Up - 100Mbps/Full - flow control rx/tx
IPv6: ADDRCONF(NETDEV_CHANGE): eth0: link becomes ready
chpasswd: password for 'root' changed
M_SENSOR_TYPE_Init eSensor 0x112
[LIBSENSOR] :M_SENSOR_TYPE_Init E_SENSOR_TYPE_800W_IMX678
st_size=118820
sttmpelen=97196
return
sysconfiglen=118820
*****************copy read time
************func = M_FLASH_ReadBakTime, 23:8:23 hour = 17, pTime->minute = 48
FUNC: M_FLASH_Init , LINE 1744 dwTargetFramerate=25, dwBitrate 16384!
net.ipv4.igmp_max_memberships = 20
hi_osal: loading out-of-tree module taints kernel.
Module himedia: init ok
Hisilicon Media Memory Zone Manager
hi_osal 1.0 init success!
  
==========chip: hi3516av300==========
==========sensor0: imx327==========
  
==========sensor1: NULL==========FUNC:parse_sensor_clock line:224 SNS:[NULL] is not supported !
FUNC:parse_sensor_bus_type line:179 SNS:[NULL] is not supported !
hi3516cv500_base: module license 'Proprietary' taints kernel.
Disabling lock debugging due to kernel taint
load sys.ko for Hi3516CV500...OK!
load tde.ko for Hi3516CV500...OK!
load region.ko for Hi3516CV500...OK!
load gdc.ko for Hi3516CV500...OK!
load vgs.ko for Hi3516CV500...OK!
load dis.ko for Hi3516CV500...OK!
load vi.ko for Hi3516CV500...OK !
load isp.ko for Hi3516CV500...OK !
load vpss.ko for Hi3516CV500...OK!
load vo.ko for Hi3516CV500...OK!
load chnl.ko for Hi3516CV500...OK!
load vedu.ko for Hi3516CV500...OK!
load rc.ko for Hi3516CV500...OK!
load venc.ko for Hi3516CV500...OK!
load h264e.ko for Hi3516CV500...OK!
load h265e.ko for Hi3516CV500...OK!
load jpege.ko for Hi3516CV500...OK!
load jpegd.ko for Hi3516CV500...OK!
load vfmw.ko ....OK!
load ive.ko for Hi3516CV500...OK!
load pwm.ko for Hi3516CV500...OK!
load hi_piris.ko for Hi3516CV500...OK!
load mipi_rx driver successful!
Load hi_cipher.ko success.
Hisilicon Watchdog Timer: 0.01 initialized. default_margin=60 sec (nodeamon= 0)
hiwtdg init ok. ver=May 28 2020, 11:04:35.
[DEV DEBUG] : GPIO Init... 0
[DEV DEBUG] : HI3516AV300 GPIO Init...
jean gpio HI_GPIO10_4
[DEV DEBUG] : HI3516AV300 GPIO Init... OK
Set LED Ctrl Mode:LEVEL
*** Board tools : ver0.0.1_20121120 ***
[debug]: {source/utils/cmdshell.c:168}cmdstr:himm
0x120101BC: 0x01802802 --> 0x01800982
[END]
[planB.c,272] sadp recvfrom errno: 100
recvfrom:: Network is doIPv6: ADDRCONF(NETDEV_UP): eth0: link is not ready
wn
[planB.c,266] waiting...
hisi-femac 10010000.ethernet eth0: Link is Up - 100Mbps/Full - flow control rx/tx
IPv6: ADDRCONF(NETDEV_CHANGE): eth0: link becomes ready
route: SIOCADDRT: File exists
-------------add_default_eth0_route-----------
M_NETPROT_Server_Start ... MaxFrameSize 3145728, nVBufferCount 6144
---------------nTimeval = 190
M_SENSOR_TYPE_Init eSensor 0x112
[LIBSENSOR] :M_SENSOR_TYPE_Init E_SENSOR_TYPE_800W_IMX678
ISP Lib Make Time Jul 11 2023 18:44:08
[LIBSENSOR] :Init imx678 OK!
...size Width=3840
...size Height=2160
nFreq 1, wdr = 1
Start Vi Dev nMainWidth 3840, nMainHeight 2160
ANV_Common_ViStartIsp : 0
---------ISP----------- FrameRate:25.00
linear mode
-------Sony IMX678 Sensor 4K@30 12bit Initial OK!-------
create isp chn 0
[ANV_Hi3516AV300_ViStartVpss-2112] ... Main:[3840,2160],Min:[1280,720]
**********Hi3516AV300 func = ANV_Hi3516AV300_VI_BindVpss
[LIBANV] : [arch/3516av300/anv_3516AV300_md.c, 672]mm = 0 (0)mask handle = 16777215 16777215 16777215 16777215
Auto PWM Init ...
Set LED Ctrl Mode:LEVEL
Set HI3516DV300/HI3516CV500 Scene Param!! Mask:0xffffffff
stExpStatistic.u8AveLum=128
AutoIris : 0
lowFarmeRate = 1
Set HI3516DV300/HI3516CV500 Sensor Param!! Mask:0xffffffff
AutoExposureEx : 0 wExpTimeMax :12
-------- MaxSysGain : 128
--------- AutoDGainMax :128
--------- AutoDGainMax :128 u32Max:131072
[DEV DEBUG] : WIFI TYPE: 0 !!
[DEV ERR] : wifi not exist !!
[LIBANV] : -------------- nVol : 12 ----------
open /appfs/soft/upnpinfo Error!
[DEV DEBUG] : 4G Device Init ...
[DEV DEBUG] : 4G Watch Task Start ...
evice eth0 entered promiscuous mode
[0m[DEV DEBUG] : 4G Watchxipc uses obsolete (PF_INET,SOCK_PACKET)
Task Start ...
Not Supported GNSS ...
[DEV DEBUG] : Device_Serial_ConfigUART 1, 9600
#############dwAFLensType 1, dwCom 0
random: fast init done