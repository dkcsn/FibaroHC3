# FibaroHC3
This file is an QA for controlling the Broadlink RM4 Pro QA.

1. first download Broadlink RM4 Pro QA, see below.
2. Install this QA - i Updated the test file from Darren_Teh https://forum.fibaro.com/topic/50287-hc3-broadlink-hub-with-support-rm4/?do=findComment&comment=226593
3. learn the Ir/Rf Codes - with https://github.com/t0mer/broadlinkmanager-docker (former versions will NOT WORK with RM4 Pro)
4. Or Use Home Assistant, Developer tools, Services to learn the codes.
    My services looked like this
    
    service: remote.learn_command
    data:
 device: GardinChannel_01
  command: opper
  command_type: rf
target:
  device_id: 476849a16e4e75fba490e7de8f7481b1
  entity_id: remote.wi_fi_universal_remote_remote
  
and look in the file config/.storage/broadlink_remote_a043b018b2ea_codes for the scanned/learned Data
  
I got it working with 433Mhz RF blinds from Jysk.dk called Huglo.

the Broadlink RM4 Pro QA is made by 10der and can be dowbloaded from here 
https://forum.fibaro.com/topic/50287-hc3-broadlink-hub-with-support-rm4/?do=findComment&comment=220161

Please be ware this QA searches for the Broadlink RM4 Pro QA by NAME, and the 10der Broadlink QA should be renamed to "Broadlink RM4 Pro" to work 

In the Broadlink mobile APP. you need to go into the app under the Broadlink device and deselect "Lock device". if not done, the Broadlink RM4 Pro QA will fail authentication.



