# yubikey-helpers
My helpers for using YubiKey

I wanted YubiKey to set keymap properly to US on insert an lock screen on removal.

Copy 70-yubikey.rules to /etc/udev/rules.d/70-yubikey.rules. And copy yubikey-udev-helper to /usr/lib/udev

This is tested on Fedora 23 with some newer YubiKeys.
