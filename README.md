# conky-jinx

A minimal [Conky](https://github.com/brndnmtthws/conky) curses theme, to be displayed on a phone-size terminal.


# Rationale

The objective of conky-jinx is to have a small text-base system monitor which draw
your attention when a core resource starts missing on a remote computer.

It is designed to fit a terminal having a width of 59 characters,
and a height of 35 characters, which is the size of [Termux](https://github.com/termux/termux-app)
running on my [Fairphone](https://www.fairphone.com) with a readable font.

![Conky-jinx screenshot](https://raw.githubusercontent.com/nojhan/conky-jinx/main/conky-jinx_screenshot.png)


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
