lsi-sata-fuckup
===============

Demo script to prove unstability of LSI-based SAS HBA with SATA-drives in enclosures.

Preconditions:
1) Use SAS expander (enclosure)
2) Use SAS HBA
3) Use SATA HDD (not SSD)


Usage:

1) Select two disks attached to same SAS-host (port in HBA), for example two drives in same expander.
2) Run script against one disk (lsi-sata-fuckup /dev/sdx)
3) Check if /dev/sdy is available (hint: it is not, like all other disks one the same SAS-host) 

WARNING: 
Cause problems with host stability. Never use in production or without ability to reboot host freely.

100% kills all data on selected drive.

USE ON PWN RISK.

