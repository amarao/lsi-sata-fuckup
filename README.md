lsi-sata-fuckup
===============

Demo script to hang LSI-based SAS HBA with SATA-drives.

Usage:

1) Set up LSI (f.e. Falcon 2008) HBA with SATA drives.
2) run lsi-sata-fuckup /dev/sdc.
3) Got all drives, attached to LSI HBA hanged.

WARNING: 
100% cause problems with host uptime, 
100% kill all data on victim drive (/dev/sdc).

USE ON PWN RISK.

