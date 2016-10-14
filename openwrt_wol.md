## howto Wake-on-Lan (wol) with your openwrt-Router

forget about the howto's on openwrt.org, they dont worked for me at all.


### install etherwake

login in your openwrt device and execute this commands:

```
#opkg update
#opkg install etherwake
```

### Test etherwake

if your target device (the maschine we want to wake up) proberly for wol configured, 
you can wake the device up with the following command.

Note: i assumed, yout default lan-interface is "br-lan". 
Replace the "xx:xx:xx:xx:xx:xx" with MAC-Address of target device.

```
#etherwake -D -i "br-lan" "xx:xx:xx:xx:xx:xx"
```
