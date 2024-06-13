
```bash
# serial ports, checked individually
dtoverlay uart0-pi5 # serial1, /dev/ttyAMA0
dtoverlay uart3-pi5 # serial4, /dev/ttyAMA3
dtoverlay uart4-pi5 # serial5, /dev/ttyAMA4
dtoverlay uart2-pi5 # serial3, /dev/ttyAMA2

# i2c-6: bar30 and friends
dtoverlay i2c-gpio i2c_gpio_sda=22 i2c_gpio_scl=23 bus=6 i2c_gpio_delay_us=0

# i2c1: ADS1115, AK09915, BME280
dtoverlay i2c1-pi5 baudrate=400000

# i2c3: PCA
dtoverlay i2c3-pi5 baudrate=400000

# SPI1: MMC5983
dtoverlay spi1-3cs

dtoverlay spi0-led

echo 597 > /sys/class/gpio/export
echo out > /sys/class/gpio/gpio597/direction
```



![[Pasted image 20240510162846.png]]