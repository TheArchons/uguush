# uguush

command-line uploader for various file hosts

![Usage](https://i.fiery.me/qqJ1.png)

## Usage

uguush [options]

Options:

`-d` Delay the screenshot by the specified number of seconds.

`-f` Take a fullscreen screenshot.

`-h` Show this help message.

`-o <host>` Select which host to use (uguu, teknik, 0x0 or fiery).

`-p <path>` Custom path to save the image to. Saves the image as "%Y-%m-%d %H-%M-%S.png".

`-c` Copy image instead of URL to clipboard.

`-n` Enable save notification (if used alongside -p option).

`-s` Take a selection screenshot.

`-u <file>` Upload a file.

`-x` Do not notify dbus, update the log, or modify the clipboard.

`-w` Take a screenshot of the current window.

`-S` Select a shortener to use (waaai or 0x0).

`-l <url>` Upload the file at the provided URL.

`-k` Use KDE/Spectacle (with -p file name will be "Screenshot_%Y%m%d_%H%M%S.png").

`-t <token>` Set token (for fiery host).

`-a <id>` Set numerical ID of an album (for fiery host).

`-D <domain>` Set custom fiery domain (only the hostname without protocol).

## Custom fiery domain

safe.fiery.me have some custom domains which redirects to i.fiery.me (the domain which serve all the files uploaded into safe.fiery.me), such as:

- nekos.will-always-want.me
- everyone.will-always-want.me
- [and more (the article's comments)](https://blog.fiery.me/2018/09/29/Extra-domain/)

So the `-D <domain>` option was added to automatically replace i.fiery.me with your desired domain (e.g. `-D nekos.will-always-want.me`).

Keep in mind that the domains will only redirect to the actual file in i.fiery.me instead of masking the original URL.

## Screenshot tool requirements

You need to have ANY (not ALL) of the following tools:

- [maim](https://github.com/naelstrof/maim) & [slop](https://github.com/naelstrof/slop) (default)
- scrot (fallback when maim & slop are missing)
- [KDE/Spectacle](https://www.kde.org/applications/graphics/spectacle/) (if using `-k` option)

## Requirements

- curl
- libnotify (for notifications)
- xclip (for clipboard support)
- xdotool (for current window capture, not needed if using `-k` option)

## Todo

## Credit

Huge thanks to all [GitHub contributors](https://github.com/jschx/uguush/graphs/contributors).

Big thanks to [neku](https://github.com/nokonoko) for creating pomf and uguu!

Inspired by [onodera-punpun](https://github.com/onodera-punpun)'s pomf.sh.

Original upload functionality by [KittyKatt](https://github.com/KittyKatt).
