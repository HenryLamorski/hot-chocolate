## how to wakeup debian machine with wol (wake-on-lan)

install ethtool, it configures your nic for wol abillity


```
#apt-get install ethtool
```


configure nic for wol abillity
```
#ethtool -s p10p1 wol g
```

after reboot, the settings are supended.
Therfore we execute this command on startup, so we edit /etc/rc.local and add:

```
ethtool -s p10p1 wol g
``` 
