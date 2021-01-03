# Wake Mobile

Proof-of-concept alarm app that uses systemd timers to wake up the system

The user needs to be logged in. Meant to be used with Phosh where this is always the case and where the system suspends after inactivity.

A setuid helper binary is used to write systemd timer drop-in unit files for the user because only system timers can wake the system up from suspend.

Installation:

```
sudo apt install gcc make
make install
```

Deinstall:

```
make uninstall
```


History: I wrote this originally for the OpenMoko where it relied on calling `rtcwake` through `pkexec` and now adapted it to show how GNOME Clocks could make use systemd timers.