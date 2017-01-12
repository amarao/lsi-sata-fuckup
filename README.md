lsi-sata-fuckup
===============

This is demo script to prove instability of LSI-based SAS HBA with SATA-drives in SAS-enclosures.

It will put any application attempting to access 'second disk' into D+ (TASK\_UNINTERRUPTIBLE) state.

Conditions:
- Use SAS expander (enclosure)
- Use SAS HBA (LSI)
- Use SATA HDD (not SSD) with queue depth > 1

Usage:

- Select two disks attached to same SAS-host (port in HBA), for example two drives in same expander (/dev/sdx, /dev/sdy)
- Run script against one disk (`lsi-sata-fuckup /dev/sdx`)
- Check if /dev/sdy is available (please note: you may have sata disks, attached to motherboard's SATA-HBA, they will continue to work, only SAS-attached driver will be affected). Example: `dd if=/dev/sdy of=/dev/null bs=1k count=1`

WARNING
-------

Cause problems with host stability. Never use in production or without ability to reboot host freely.

100% kills all data on selected drive.

USE ON PWN RISK.

