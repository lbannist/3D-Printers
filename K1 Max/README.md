Start by going to https://3dfilamentprofiles.com/filaments/ and find the filament profile you are looking for.  It should provide you will a information about temperature ranges

I used Elgoo Black PLA
Temp at 225oC (220 was ok, but had too many faliures
Bed at 55oC (60 is also good, but between this and the nozzle, I am trying to prevent/slow any heat creep issues)
Max Volumetric Flow set to 12 mm3/s
Cooling (Lowered model fan speed due to the theory that 100% = 12000rpm is overpowering the nozzle's ability to heat the PLA.   For reference, Ender 3's 100% is at 7000 rpm.  Also turned the aux fan off and the back exhaust off).  First Layer at 50% and Others Layers at 70%

Bed Temp - If not provided, PLA @ 55oC is a good starting point because that is the glass temperature of PLA, at which PLA starts cool down and take its final solid shape.  If you can keep the temperature at or above that temperature, then the PLA will be held just a little too high to fully solidify.

--- Temperature Tower
I could get 220C but nothing lower.  But then tried flow test and it couldn't even get to all the outside edges on the first layer before clogging.
So I upped the nozzle temperature to 225C and proceeded to the Flow Rate Calibration.



--- Flow Rate
Follow the normal 2 step procedure.
Pass #1 (Flow @ 0.98) - This pass went well and showed smoothness up around +10 and +15, so I used +15, which translates to a flow of 1.127 (0.98*(100+15)/100).  Side note, I did notice spikes in max volumetric flow rate where unretraction took place, so my theory is that this is due to pressure advance of 0.03, not a big deal since its nearly instantaneous, but if the volumetric flow is already way ove 12, a further spike could cause the nozzle clogging that I noticed before calibation.
Pass #2 (Flow @ 1.127) - Failed at L2 (starting at -7 tile) and produced a max volumetric flow of 15.63 mm3/s
Pass #2 (Flow @ 1.078) - Failed at L4 (starting at -7 tile)  This Flow is a +10 and produced a max volumetric flow of 14.88 mm3/s
Pass #2 (Flow @ 1.045) - Success, but with very slight underextrusion (only partially on the tile) at the top layer.  Best of the group were #0, #2, and #3.  So I used #3.   This flow value was determined by 1.078(100-3)/100 and produced a max volumetric flow of 14.38 mm3/s
Pass #2 (Flow @ 1.0241) - Success, but only did tiles #0 to #4 because #5 would put the flow below 0.98, which makes no sense to test at this time.  All 4 tiles were amazing, no stringing, but the top layers looked uniformally underextruded.   Thoery - The line width during the test is 0.48, but my process profile has top and internal solid set to 0.42.  This flow value was determined by 1.045(100-2)/100  and produced a max volumetric flow of 13.81 mm3/s.  For reference, Pass #1 +5 would have a flow rate of 1.029

Going to try to force 0.45 and rerun the test (or a #0 tile similar and see what happens).  If that does not work, then force 0.42 as per the profile and see if that closes up the gap.

