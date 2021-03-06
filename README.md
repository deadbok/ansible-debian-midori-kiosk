# Ansible role to install the Midori web rowser in kiosk mode on Debian

 * Install and configure Plymouth boot splash screen.
 * Install Xorg, matchbox VM, and Midori
 * Auto login as configurable user and run Midori

## Compatibility

 * Debian 9 (stretch)

## Variables

### States of packages and services

 * **kiosk_packagess_state** (*installed/latest*): Whether to make sure the latest packages are installed (default: latest)

### Boot process

 * **grub2_graphics_mode** (*string*): Grub2 graphics mode (default: "1024x768x32")
 * **grub2_stable_netnames** (*boolean*): Use stable inteface names. Disable when using vagrant (default: true)
 * **initramfs_modules** (*list*): Modules to load in the initramfs (graphics drivers for plymouth) (default:  "intel_agp", "drm", "i915 modeset=1")
 * **plymouth_theme** (*string*):  Theme for plymouth the splash screen (default: solar)
 * **autologin_user** (*string*): User running the kiosk mode processes  (default: vagrant)
 * **autologin_group** (*string*): Group running the kiosk mode processes  (default: vagrant)
 * **kiosk_user_home_dir** (*string*): Home directory of the kiosk mode user (default: /home/vagrant)

### Midori

 * **kiosk_url** (*installed/latest*): URL to open in Midori (default: https://groenholdt.net)
 * **kiosk_reload_url_seconds** (*installed/latest*): Continuously reload URI after this many seconds  (default: 30)
 * **kiosk_command** (*string*): Command to run after system boot to X.
