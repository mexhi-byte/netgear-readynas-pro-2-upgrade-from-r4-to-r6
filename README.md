I found an old Netgear ReadyNAS Ultra 2 from many years ago and wanted to upgrade it to the latest version of firmware. The ReadyNAS said the latest version was RAIDiator 4.2 however when I visited Netgear's support site, it appeared as though they released an entirely new OS called ReadyNAS OS - the latest version was 6.10.3.

Some internet searching told me that it was possible (although, completely unsupported by Netgear), and I found several directions (links below in the "Resources" section) on how to perform the upgrade to ReadyNAS OS 6.* - below are the steps I followed for posterity, as well as the binary files used (mostly because I had a hard time finding them, most of the links I found pointed to Netgear's site, but the links / files had since been removed - fair, since they were from 2015 and that was a while ago).

Prerequisites:

A BACKUP OF YOUR DATA! This will delete all data on the NAS, and it's never a bad idea to have tested backups! THESE STEPS WILL DELETE ALL THE DATA ON YOUR NAS! (I take no responsibility for anything that happens to your data, follow at your own risks.)
A ReadyNAS
Two files, a 'prep' file, and the upgrade file
R4toR6_Prep_Addon.bin - this file sets up the NAS to perform a factory reset at the appropriate point during the upgrade
R4toR6_6.9.5.bin - this file is the binary to perform the upgrade
Below are the md5 checksums for both files:

> md5sum *.bin

1c3d9f17903c3918fd882c9fc2eb2802  R4toR6_6.9.5.bin

7278abf53f7d803e2f1791549f95ecc4  R4toR6_Prep_Addon.bin


I have posted these files on my GitHub for posterity, including the above md5 checksums for verification.


Steps:

1) Navigate to "Add-ons -> Add New"

2) "Choose file" and select the "R4toR6_Prep_Addon.bin" file

3) Click "Upload and verify image..."



4) Once the file is uploaded and verified successfully, you will see the below; click "Install"



5) You might be prompted to restart - do not restart.

6) Navigate to "System -> Update -> Local"

7) "Choose file" and select the "R4toR6_6.9.5.bin" file



8) Click "Upload and verify image..."

9) Click "Perform System Update", when prompted select "Shutdown and reboot device."



10) Wait about 5 - 10 minutes - the NAS will be rebooted and you will be able to connect to the web interface, having had a factory reset as part of the process, the credentials will now be "admin/password" and you will be prompted to change this upon login.



11) Configure as desired, and enjoy the newer version!
