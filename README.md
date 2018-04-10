uguush
========

command-line uploader for various file hosts

![Usage](https://u.teknik.io/WldwN2.png)

Usage
-----

uguush [options]

Options:

`-d` Delay the screenshot by the specified number of seconds.

`-f` Take a fullscreen screenshot.

`-h` Show this help message.

`-o` Select a host to use. Can be uguu, teknik, 0x0, ptpb, maxfile, or mixtape.

`-s` Take a selection screenshot.

`-u <file>` Upload a file.

`-w` Take a window screenshot.

`-x` Suppress communications: Do not log, modify clipboard, or notify DBUS.

`-S` Select a shortener to use. Can be waaai, ptpb, or 0x0.

`-i` Apply shadow effect to window screenshot using ImageMagick.

`-l` Re-upload the given url.

`-p <path>` Custom path to save the image to. Saves the image as "%Y-%m-%d %H-%M-%S.png"

`-k` Use Spectacle of KDE Plasma.

Requirements
------------

- curl
- libnotify (for notifications)
- maim (for screenshot)
- slop (for selection capture)
- xclip (for clip-board support)
- xdotool (for current window capture)
- ImageMagick (optional, only for `-i` option)
- Spectacle (optional, only for `-k` option)

Todo
----

POSIX sh compliance.

Credit
------

Big thanks to [neku](https://github.com/nokonoko) for creating pomf and uguu!

Inspired by [onodera-punpun](https://github.com/onodera-punpun)'s pomf.sh.

Original upload functionality by [KittyKatt](https://github.com/KittyKatt).

**New** upload functionality and refactoring by [arianon](https://github.com/arianon).

Various features and help from [DanielFGray](https://github.com/DanielFGray).
