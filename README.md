Flsun default 1.3 branch with tramming aka leveling renabled. so mesh "works" 
Keep inn mind Klipper screen does not use "probe_calibrate" and, is unable to save "probe offsets" this leads to large "babysteps aka zoffset in mainsail" 
it will be required to solve this running the ommand from "terminal/console" in mainsail"  you must type "accept" first before running "save_config" 
check the bottom of printer.cfg for the new zoffset. 
-2. you now must run , delta_calibrate to apply the new "probe" offset" and, also "tramm" the effector to the bed. 
The last step is to run bed_mesh. 
this order of events is absolute failure to do so will lead into offsets not being applied or general scrapes / other issues. this is the correct "offical website method" 
general_disclaimer this is just a quick patch/bandaid. for a quick option/solution 

The recoomend is. to also reinstall "klipperScreen" returning it to normal commands / layout. e.g it has a automated button to set probe_calibrate under "zcalibrate"  click on "probe" to run this. then use the buttons 
to get the correct offset. 

Finally everything else can be left as is avoiding further hastle. 


steps to install. 

Must have v1.3 firmware. (most pads out of box are 1.1) and, have no ssh.  back up anything you care about incase. 

open terminal/cmd on pc. 

type ssh , pi@speeder-pad.local  or, ssh pi@ipadress. 

type ls enter you should see klipper folder 

sudo rm -r klipper enter 

gitclone https://github.com/danorder/klipper_fs-stock-pad.git enter 

sudo service klipper restart enter 

Relevel printer carry on. 
 


