This page is where problems and solutions are written



# TROUBLESHOOTING

## PROBLEM - All of a sudden, mainsail cannot find the connected 3D Printers ***

1. Check to see if the printers are still actually connected.  
If so, open Linux Terminal and type **ping** 10.140.4.65:7125 , and press **Enter**.  The terminal window  will then grind through all the ports from 10.140.4.65:0001 to whatever.   I choose to close the terminal window at around 1600 since I already knew the port was going to be 7125.
If it does not show the same IP as what you entered (i.e. 10.140.7.300), chances the PC renewed the 3D printers IP addresss (common background function that ever PC does on a regular basis [i.e. once per month])
2. Update the IP address of the printers with the new IP address and the old port (i.e. 10.140.7.300:7125) and Mainsail should now connect.

### Now that Mainsail can connect
If Mainsail can connect, but the Klipper is not working, chances are the USB name changed as you were troubleshooting (i.e. from ttyUSB1 and is not sohwing ttyUSB3)

3. Go to printer.cfg, around line 87 there is a USB reference that needs to be updated to the new USB name.  Then save the .cfg and the printer should be good (might need to be rehomed).

### Now that the PC can connect to the printer via Mainsail/Klipper
4. Try STEPPER_BUZZ which will just cause the head to move back and forth just enough to buzz (so do it in a quiet room).  Fix any ttyUSB reference in printer.cfg .A mismatch could destroy a printer's build plate as the nozzle comes crashing down into the build plate while homing.
5. Rehome to verify that the correct ttyUSB is for the correct printer.
6. Update the IP address in any PC that sends prints over the network.
