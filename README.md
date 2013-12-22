# powersave

Arch Linux Powersave package for Dell Inspiron 7000 (7537)

## bin/powersave

This script changes some kernel variables in order to save power.

You can call this sript directly by issuing

    powersave true  # to activate power saving
    powersave false # to disable power saving

## rules.d/50-powersave.rules

udev rules to trigger powersave with proper parameter if plugged on unplugged.
