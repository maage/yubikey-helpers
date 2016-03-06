# yubikey-helpers
My helpers for using YubiKey

I wanted YubiKey to set keymap properly to US on insert an lock screen on removal.

Add these to /etc/udev/rules.d/70-yubikey.rules. And copy yubikey-udev-helper to /usr/lib/udev

```
ACTION=="add|change|remove", \
   SUBSYSTEM=="usb", \
   ATTRS{idVendor}=="1050", \
   ATTRS{idProduct}=="0010|0110|0111|0113|0114|0115|0116|0120|0401|0402|0403|0405|0406|0407|0410", \
   RUN+="/usr/lib/udev/yubikey-udev-helper"
 ```
 This is tested on Fedora 23.
