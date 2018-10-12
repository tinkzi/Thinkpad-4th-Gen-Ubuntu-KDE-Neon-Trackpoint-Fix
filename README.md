# Thinkpad-4th-Gen-Ubuntu-KDE-Neon-Trackpoint-Fix


Trackpoint mouse fix for my Thinkpad t540p and x240 on ubuntu 16.04(and flavors) and KDE Neon.
Just copy xorg.conf.d files to /usr/share/X11/

==========================================================================================

#If you find trackpint mouse glitchy then set it to flat:

nano ~/.profile

Add the following line at the bottom of the text file.

xinput --set-prop (xinput ID) 'libinput Accel Profile Enabled' 0, 1.





Use xinput list on terminal to get your trackpoint number, in my case id is 12 , example




computer@example $ xinput list






 Virtual core pointer                          id=2    [master pointer  (3)]
  ↳ Virtual core XTEST pointer                id=4    [slave  pointer  (2)]
   ↳ SynPS/2 Synaptics TouchPad                id=11   [slave  pointer  (2)]
   ↳ TPPS/2 IBM TrackPoint                     id=12   [slave  pointer  (2)]
 Virtual core keyboard                         id=3    [master keyboard (2)]
    ↳ Virtual core XTEST keyboard               id=5    [slave  keyboard (3)]
    ↳ Power Button                              id=6    [slave  keyboard (3)]
    ↳ Video Bus                                 id=7    [slave  keyboard (3)]
    ↳ Sleep Button                              id=8    [slave  keyboard (3)]
    ↳ Integrated Camera: Integrated C           id=9    [slave  keyboard (3)]
    ↳ AT Translated Set 2 keyboard              id=10   [slave  keyboard (3)]
    ↳ ThinkPad Extra Buttons                  
    
    
    
    
    
    
=================================================================================================





#If you find mouse sensitivity very slow, use mouse and touchpad on settings or use this command below and put it in ~/.profile:

xinput --set-prop 12 'libinput Accel Speed' (your speed) example:

xinput --set-prop 12 'libinput Accel Speed' 0.7

