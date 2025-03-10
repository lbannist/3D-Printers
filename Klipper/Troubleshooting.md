This page is where problems and solutions are written




*** PROBLEM - All of a sudden, mainsail cannot find the connected 3D Printers ***

Check to see if the printers are still actually connected.  
If so, open Linux Terminal and type ping 10.140.4.65:7125 , and press Enter
The terminal window  will then grind through all the ports from 10.140.4.65:0001 to whatever
If it does not show the same IP as what you entered (i.e. 10.140.7.300), chances the PC renewed the 3D printers IP addresss (common background function that ever PC does on a regular basis [i.e. once per month])
Update the IP address of the printers with the new IP address and the old port (i.e. 10.140.7.300:7125) and Mainsail should now connect.

If Mainsail can connect, but the Klipper is not working, chances are the USB name changed as you were troubleshooting (i.e. from ttyUSB1 and is not sohwing ttyUSB3)
Go to printer.cfg, around line 87 there is a USB reference that needs to be updated to the new USB name.  Then save the .cfg and the printer should be good (might need to be rehomed).

Rehome to verify that the correct ttyUSB is for the correct printer.  I mismatch could destroy a printer's build plate as the nozzle comes crashing down into the build plate while homing.
