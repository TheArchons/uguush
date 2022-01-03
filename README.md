# uguush

command-line uploader for various file hosts

![Usage](https://i.fiery.me/NaSQ.png)

## Usage

uguush [options]

Options:

`-d` Delay the screenshot by the specified number of seconds.

`-f` Take a fullscreen screenshot.

`-h` Show this help message.

`-o <host>` Select which host to use (`uguu`, `teknik`, `0x0` or `fiery`).

`-p <path>` Custom path to save the image to (saves as `%Y-%m-%d %H-%M-%S.png`).

`-c` Copy image instead of URL to clipboard.

`-n` Enable save notification (if used alongside `-p` option).

`-s` Take a selection screenshot.

`-u <file>` Upload a file.

`-x` Do not notify dbus, update the log, or modify the clipboard.

`-X` Skip upload.

`-w` Take a screenshot of the current window.

`-S <shortener>` Select a shortener to use (`waaai` or `0x0`).

`-l <url>` Upload the file at the provided URL.

`-g` Use gnome-screenshot (with `-p` saves as `Screenshot from %Y-%m-%d %H-%M-%S.png`).

`-k` Use KDE/Spectacle (with `-p` saves as `Screenshot_%Y%m%d_%H%M%S.png`).

`-t <token>` Set token (for `fiery` host).

`-a <id>` Set numerical ID of an album (for `fiery` host).

`-D <domain>` (DEPRECATED) Set `safe.fiery.me` file domain.

`-F <domain>` Set fiery host domain.

## Screenshot tool requirements

You need to have ANY (not ALL) of the following tools:

- [maim](https://github.com/naelstrof/maim) & [slop](https://github.com/naelstrof/slop) (default)
- scrot (fallback when maim & slop are missing)
- [KDE/Spectacle](https://www.kde.org/applications/graphics/spectacle/) (if using `-k` option)
- [GNOME/Screenshot](https://apps.gnome.org/app/org.gnome.Screenshot/) (if using `-g` option)

## Requirements

- curl
- libnotify (for notifications)
- xclip (for clipboard support)
- xdotool (for current window capture, not needed if using `-k` or `-g` options)

## Fiery host domain

This allows using any [lolisafe (v3)](https://github.com/WeebDev/chibisafe/tree/v3.0.0) or forks of [BobbyWibowo/lolisafe](https://github.com/BobbyWibowo/lolisafe).

`-o` option must be set to `fiery` since otherwise the script will default to `uguu` file host.

```bash
uguush -s -k -o fiery -F my.lolisafe.domain
```

Can optionally set protocol if required (e.g. `-F "http://my-unsafe.lolisafe.domain"`)

## safe.fiery.me file domain (DEPRECATED)

Read more about this at: [https://blog.fiery.me/update-about-will-always-want-me](https://blog.fiery.me/update-about-will-always-want-me).

```bash
uguush -s -k -o fiery -D your-hot-neighbor.will-always-want.me
```

Keep in mind that the domains will only redirect to the actual file in `i.fiery.me` instead of masking the original URL.

Though it should work pretty well with chat apps that allow link previews (e.g. Discord).

## Todo

- [ ] N/A

## Credit

Huge thanks to all [GitHub contributors](https://github.com/jschx/uguush/graphs/contributors).

Big thanks to [neku](https://github.com/nokonoko) for creating pomf and uguu!

Inspired by [onodera-punpun](https://github.com/onodera-punpun)'s pomf.sh.

Original upload functionality by [KittyKatt](https://github.com/KittyKatt).
