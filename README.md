# powersave

Arch Linux Powersave package for Dell Inspiron 7000 (7537)

Please note that this might not work on your system so check what it's doing
before you apply those settings to your machine.

## bin/powersave

This script changes some kernel variables in order to save power.

You can call this script directly by issuing:

    powersave true  # to activate power saving
    powersave false # to disable power saving

## rules.d/50-powersave.rules

`udev` rules to trigger powersave with proper parameter if plugged on unplugged.
