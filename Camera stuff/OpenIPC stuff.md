

steps:

- download everything
- open hitool
- go to burn tool
- setup network and serial port stuff
- click "browse" and pick the xml file
- click burn
- re-plug the power to the camera within 15 seconds
- wait
- open the serial at 115200
- run:
```setenv bootargs 'mem=512M console=ttyAMA0,115200 root=/dev/mtdblock2 rootfstype=squashfs mtdparts=hi_sfc:1M(boot),2M(kernel),13M(rootfs)'

setenv bootcmd 'sf probe 0;sf read 0x82000000 0x100000 0x200000;bootm 0x82000000' 

saveenv
```
- re-plug power


### debugging:
it turned out that fw_env.config was missing. it's content needs to be:
```
/dev/mtd0 0x80000 0x40000
```




setenv bootargs 'mem=512M console=ttyAMA0,115200 root=/dev/mtdblock2 rootfstype=squashfs init=/init mtdparts=hi_sfc:1M(boot),2M(kernel),10M(rootfs),-(rootfs_data)

setenv bootcmd 'sf probe 0;sf read 0x82000000 0x100000 0x200000;bootm 0x82000000' 


![[Pasted image 20231115002509.png]]https://forum.archive.openwrt.org/viewtopic.php?id=28454

if we change mem to 128 in bootargs, we can run `load3516av300 -i -sensor0 imx327 -osmem 128 ` script after copying it to /lib/modules/.../hisilicon/

that does not result in a segfault =]

fw_setenv sensor imx327
fw_setenv totalmem 512
fw_setenv osmem 128


https://kojenov.com/2020-09-15-hisilicon-encoder-vulnerabilities/#5150---serial-to-tcp


for tomorrow:
 add this to load3516av300:
 
echo 'root:batata' | chpasswd

remove bootdelay

flash and have fun

