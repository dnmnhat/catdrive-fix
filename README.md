# catdrive hardwhare control

THIS ONLY APPLY TO CATDRIVE RUNING DSM7.0

THIS ONLY APPLY TO CATDRIVE RUNING DSM7.0

THIS ONLY APPLY TO CATDRIVE RUNING DSM7.0


EVERY COMMAND BELOW MUST BE EXECUTED AS ROOT

EVERY COMMAND BELOW MUST BE EXECUTED AS ROOT

EVERY COMMAND BELOW MUST BE EXECUTED AS ROOT


each of the following section of command must be executed with the following combinitation otherwies things are goinf to get messed up

each section of command can be added to task scheduler to perform different notification





# red led
```sh
i2cset -y -f 0 0x45 0x00 0x55
i2cset -y -f 0 0x45 0x01 0x01
i2cset -y -f 0 0x45 0x31 0x03
i2cset -y -f 0 0x45 0x32 0x03
i2cset -y -f 0 0x45 0x33 0x03
i2cset -y -f 0 0x45 0x30 0x07

i2cset -y -f 0 0x45 0x34 128
i2cset -y -f 0 0x45 0x35 0
i2cset -y -f 0 0x45 0x36 0
```




# green led
```sh
i2cset -y -f 0 0x45 0x00 0x55
i2cset -y -f 0 0x45 0x01 0x01
i2cset -y -f 0 0x45 0x31 0x03
i2cset -y -f 0 0x45 0x32 0x03
i2cset -y -f 0 0x45 0x33 0x03
i2cset -y -f 0 0x45 0x30 0x07

i2cset -y -f 0 0x45 0x34 0
i2cset -y -f 0 0x45 0x35 128
i2cset -y -f 0 0x45 0x36 0
```

# blue led
```sh
i2cset -y -f 0 0x45 0x00 0x55
i2cset -y -f 0 0x45 0x01 0x01
i2cset -y -f 0 0x45 0x31 0x03
i2cset -y -f 0 0x45 0x32 0x03
i2cset -y -f 0 0x45 0x33 0x03
i2cset -y -f 0 0x45 0x30 0x07

i2cset -y -f 0 0x45 0x34 0
i2cset -y -f 0 0x45 0x35 0
i2cset -y -f 0 0x45 0x36 128
```

# rainbow color led
```sh
i2cset -y -f 0 0x45 0x00 0x55
i2cset -y -f 0 0x45 0x01 0x01
i2cset -y -f 0 0x45 0x30 0x07

i2cset -y -f 0 0x45 0x31 0x72
i2cset -y -f 0 0x45 0x32 0x72
i2cset -y -f 0 0x45 0x33 0x72

i2cset -y -f 0 0x45 0x37 0x44
i2cset -y -f 0 0x45 0x3a 0x55
i2cset -y -f 0 0x45 0x3d 0x66

i2cset -y -f 0 0x45 0x38 0x44
i2cset -y -f 0 0x45 0x3b 0x55
i2cset -y -f 0 0x45 0x3e 0x66
i2cset -y -f 0 0x45 0x39 0x40
i2cset -y -f 0 0x45 0x3c 0x40
i2cset -y -f 0 0x45 0x3f 0x40

i2cset -y -f 0 0x45 0x34 128
i2cset -y -f 0 0x45 0x35 128
i2cset -y -f 0 0x45 0x36 128
```




# small catdrive: yellow led, big catdrive: brown led
```sh
i2cset -y -f 0 0x45 0x00 0x55
i2cset -y -f 0 0x45 0x01 0x01
i2cset -y -f 0 0x45 0x31 0x03
i2cset -y -f 0 0x45 0x32 0x03
i2cset -y -f 0 0x45 0x33 0x03
i2cset -y -f 0 0x45 0x30 0x07

i2cset -y -f 0 0x45 0x34 128
i2cset -y -f 0 0x45 0x35 128
i2cset -y -f 0 0x45 0x36 128
```

# led off
```sh
i2cset -y -f 0 0x45 0x00 0x55
```

# big catdrive poweroff
```sh
/usr/bin/systemctl --force poweroff
i2cset -y -f 0 0x45 0x77 0xc6
sleep 1
reboot
```

# small catdrive poweroff
```sh
/usr/bin/systemctl --force poweroff
i2cset -y -f 0 0x45 0x00 0x55
i2cset -y -f 0 0x45 0x01 0x01
i2cset -y -f 0 0x45 0x31 0x33
i2cset -y -f 0 0x45 0x32 0x33
i2cset -y -f 0 0x45 0x33 0x33
i2cset -y -f 0 0x45 0x30 0x07
i2cset -y -f 0 0x45 0x34 128
i2cset -y -f 0 0x45 0x35 0
i2cset -y -f 0 0x45 0x36 0
```
