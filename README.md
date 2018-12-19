# uguush

command-line uploader for various file hosts

![Usage](https://i.fiery.me/oJAo.png)

## Usage

uguush [options]

Options:

`-d` Delay the screenshot by the specified number of seconds.

`-f` Take a fullscreen screenshot.

`-h` Show this help message.

`-o <host>` Select which host to use (uguu, teknik, 0x0, ptpb, mixtape, lewd, fiery or doko).

`-p <path>` Custom path to save the image to. Saves the image as "%Y-%m-%d %H-%M-%S.png"

`-n` Enable save notification (if used alongside -p option).

`-s` Take a selection screenshot.

`-u <file>` Upload a file.

`-x` Do not notify dbus, update the log, or modify the clipboard.

`-w` Take a screenshot of the current window.

`-S` Select a shortener to use. Can be waaai or 0x0.

`-l <url>` Upload the file at the provided URL.

`-k` Use KDE/Spectacle (with -p file name will be "Screenshot_%Y%m%d_%H%M%S.png").

`-t <token>` Set token (only for fiery host).

`-a <id>` Set numerical ID of an album (only for fiery host).

`-D <domain>` Set custom fiery domain (only the hostname without protocol).

## Custom fiery domain

safe.fiery.me have some custom domains which redirects to i.fiery.me (the domain which serve all the files uploaded into safe.fiery.me), such as:

- nekos.will-always-want.me
- everyone.will-always-want.me
- [and more (the article's comments)](https://blog.fiery.me/2018/09/29/Extra-domain/)

So, the `-D <domain>` option was added to automatically replace i.fiery.me with your desired domain.

Do remember it's only a redirect, so when people visit the link with the custom domain, they will only be redirected to the actual file in i.fiery.me.

## Screenshot tool requirements

You need to have ANY (not ALL) of the following tools:

- [maim](https://github.com/naelstrof/maim) & [slop](https://github.com/naelstrof/slop) (default)
- scrot (fallback when maim & slop are missing)
- [KDE/Spectacle](https://www.kde.org/applications/graphics/spectacle/) (with `-k` option)

## Requirements

- curl
- libnotify (for notifications)
- xclip (for clipboard support)
- xdotool (for current window capture, optional with `-k` option)

## Todo

## Credit

Huge thanks to all [GitHub contributors](https://github.com/jschx/uguush/graphs/contributors).

Big thanks to [neku](https://github.com/nokonoko) for creating pomf and uguu!

Inspired by [onodera-punpun](https://github.com/onodera-punpun)'s pomf.sh.

Original upload functionality by [KittyKatt](https://github.com/KittyKatt).
