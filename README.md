# thinkpad-x200-coreboot
coreboot rom for thinkpad x200 featuring seabios 

it has been compiled to use libgfixnit graphics initialization

Rom is 8mb, I could compile the 4 and 16mb as well for this model but I have just a laptop and it has a 8mb chip so I will not be able to test it.

gbe.bin has been added with a random MAC address 00:11:22:33:44:55

No support to intel wifi and bluetooth

./cbfstool x200m4rc0.rom add-int -i 1000 -n etc/boot-menu-wait has been already applied to reduce the waiting time

added flashregion_0_flashdescriptor.bin from libreboot

ich9fdgbe_8m.bin with 00:11:22:33:44:55 mac address

No secondary payloads added

capable to boot any linux, bsd and windows

to flash it

sudo flashrom -p internal -w x200m4rc0.rom -V

or

sudo flashrom -p internal:laptop=force_I_want_a_brick -w x200m4rc0.rom -V

To see how this (or my others built images) works, just have a look into my youtube https://www.youtube.com/user/marcolinoxz

