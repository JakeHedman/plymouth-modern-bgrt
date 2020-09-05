
# plymouth-modern-bgrt theme

A theme for plymouth which uses your system's UEFI logo (aka BGRT). 
Based on [plymouth-bgrt](https://github.com/darac/plymouth-bgrt).

You may want to tweak your kernel parameters to have a smooth transition from the bootloader to plymouth. \
On intel graphics, this is done by passing the `i915.fastboot=1` parameter. I would advise to add it to your bootloader
AFTER testing if it works, for example in GRUB by pressing `e` to edit the boot entry for one time only.

## Screenshot

Running on my ThinkPad T440p, with a custom BIOS logo. Booting an encrypted root partition with a passphrase prompt.

![Screenshot](./preview.png)

## Installation

```sh
    sudo ./install.sh	# Fetches your BGRT, adjusts the theme to suit and installs it.
    sudo plymouth-set-default-theme -R plymouth-modern-bgrt
```

## GRUB Theme

You may also want to pair this with darac's [GRUB theme](https://github.com/darac/grub-bgrt).

If you use it, make sure that the boot_menu and the terminal don't cover your boot logo.
You can edit the theme.txt file if it does.

## License

All the files in this project are distributed under the [GNU General Public License](./LICENSE).

## Author of `plymouth-bgrt`

Paul Saunders
