# conky-jinx

A minimal [Conky](https://github.com/brndnmtthws/conky) curses theme, to be displayed on a phone-size terminal.


# Rationale

The objective of conky-jinx is to have a small text-base system monitor which draw
your attention when a core resource starts missing on a remote computer.

It is designed to fit a terminal having a width of 59 characters,
and a height of 35 characters, which is the size of [Termux](https://github.com/termux/termux-app)
running on my [Fairphone](https://www.fairphone.com) with a readable font.


# Features

Conky-jinx displays only the basic resources that generally bring troubles:

- RAM usage,
- Swap usage,
- CPU usage,
- Filesystem usage,
- I/O rates,
- Network rates.

For RAM, Swap, CPU and Filesystem, the color of the bars change depending on
their load, from white to red (going through rainbow colors).

If you spot a bar being red, bad things are probably happening.


# Install & run

```sh
sudo apt install conky-cli
git clone --single-branch main --depth 1 https://github.com/nojhan/conky-jinx.git
conky -c conky-jinx/jinx.conky
```


# Screenshot

(Without the colors)

```
- MEMORY ------------------------------------------------

    RAM: 78% ###################################_________
        6,01GiB / 7,66GiB

    SWP: 76% ##################################__________
        1,53GiB / 2,00GiB

    Top Processes:
        GeckoMain         19,96%
        Isolated Web Co    6,35%
        Isolated Web Co    6,25%
        WebExtensions      5,83%
        Isolated Web Co    5,18%


- CPU @ 1,14 GHz -----------------------------------------

    CPU: 23% ##########__________________________________
      1: 21% #########___________________________________
      2: 23% ##########__________________________________
      3: 27% ############________________________________
      4: 27% ##########__________________________________

    Top Processes (0/320):  PID     CPU     MEM
        gvfs-udisks2-vo   16859    2,28    0,05
        GeckoMain         61198    1,27   19,96
        pulseaudio        16811    1,02    0,09
        systemd               1    0,76    0,12
        dbus-daemon         866    0,76    0,05


- DISKS -------------------------------------------------

    FS: ########################################____
       420GiB / 457GiB

    IO: 2,00KiB / 1,52MiB


- NETWORK -----------------------------------------------

    ETHN: 0,5 KiB/s / 0,0 KiB/s
    WIFI: 0,0 KiB/s / 0,0 KiB/s




---------[0 > 40 > 50 > 60 > 70 > 80 > 90 > 100]---------
```
