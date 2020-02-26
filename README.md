# mugenhwcfg-live

This repository contains tooling to build a [Debian Live](https://live-team.pages.debian.net/live-manual/html/live-manual/index.en.html) system, which can be used to run the `mugenhwcfg` [tool](https://git.codelabs.ch/?p=muen/mugenhwcfg.git) in an automated fashion.

When booted, the live system will automatically run the tool and upload the output to the Debian [pastebin](http://paste.debian.net).

To build the ISO image on a Debian 10.x (buster) system with `live-build` installed, clone this repository and run:

```
sudo lb build
```

The run the ISO image under KVM/QEMU, it is sufficient to pass it to your desired `qemu` invocation using `-cdrom`.

To boot on real hardware it should be sufficient to just dump the ISO image to an USB stick, but this has not yet been tested.

Development of this tooling is sponsored by [Nitrokey GmbH](https://nitrokey.com).
