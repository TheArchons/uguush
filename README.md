# uguush

command-line uploader for various file hosts

![Usage](https://i.fiery.me/YB00.png)

## Usage

uguush [options]

Options:

`-d` Delay the screenshot by the specified number of seconds.

`-f` Take a fullscreen screenshot.

`-h` Show this help message.

`-o` Select a host to use. Can be uguu, teknik, 0x0, ptpb, mixtape, lewd, fiery or doko.

`-p <path>` Custom path to save the image to. Saves the image as "%Y-%m-%d %H-%M-%S.png"

`-n` Enable save notification (if used alongside -p option).

`-s` Take a selection screenshot.

`-u <file>` Upload a file.

`-x` Do not notify dbus, update the log, or modify the clipboard.

`-w` Take a screenshot of the current window.

`-S` Select a shortener to use. Can be waaai or 0x0.

`-i` Apply shadow effect to window screenshot using ImageMagick.

`-l <url>` Upload the file at the provided URL.

`-k` Use Spectacle of KDE Plasma (with -p file name will be "Screenshot_%Y%m%d_%H%M%S.png").

`-t <token>` Set token (only for fiery host).

`-a <id>` Set numerical ID of an album (only for fiery host).

## Requirements

- curl
- libnotify (for notifications)
- maim (for screenshot, optional if using `-k`)
- slop (for selection capture, optional if using `-k`)
- xclip (for clip-board support)
- xdotool (for current window capture)
- ImageMagick (optional, only for `-i` option)
- Spectacle (optional unless using `-k` option, in which main and slop will become optional instead)

## Todo

POSIX sh compliance.

## Credit

Huge thanks to all [GitHub contributors](https://github.com/jschx/uguush/graphs/contributors).

Big thanks to [neku](https://github.com/nokonoko) for creating pomf and uguu!

Inspired by [onodera-punpun](https://github.com/onodera-punpun)'s pomf.sh.

Original upload functionality by [KittyKatt](https://github.com/KittyKatt).
