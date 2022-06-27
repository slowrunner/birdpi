# birdpi
My implementation of BirdNet-Pi


REF:  BirdNetPi.com  
REF:  https://github.com/mcguirepr89/BirdNET-Pi  

== INSTALLATION ==  

1) Wrote PiOS Lite 64-bit  
- Host: BirdPi  

2) First Login  
- ssh-keygen -R X.X.X.X
- setup git  
  - created slowrunner/birdpi
  - sudo apt install git
  - git clone https://github.com/slowrunner/birdpi.git
  - setup git credentials

3) Increase swap space  
```
sudo dphys-swapfile swapoff
sudo nano /etc/dphys-swapfile
edit CONF_SWAPSIZE=1024
sudo dphys-swapfile setup
sudo dphys-swapfile swapon
```

4) BirdNet-Pi setup
- cd ~
- curl -s https://raw.githubusercontent.com/mcguirepr89/BirdNET-Pi/main/newinstaller.sh | bash
- browse to http://birdpi.local   <-- note: not birdnetpi.local
- Username: birdnet
- Initial pw empty - Set in Tools->Settings->AdvancedSettings
  - Audio Channels: 1
  - Password: 
  - Location: (round to to 4 decimal places)

5) Test
- Play bird from Merlin
- Tools->SystemServices->ClearAllData


== MAINTENANCE ==  

- SHUTDOWN:  Tools->SystemServices->Shutdown
- CLEARALLDATA:  Tools->SystemServices->ClearAllsData


=== PERFORMANCE ON Pi3B - OUTSIDE AIR 91degF ===
```
 17:33:17 up  5:49,  2 users,  load average: 1.90, 2.25, 2.33
               total        used        free      shared  buff/cache   available
Mem:             909         468         156           3         284         380
Swap:           1023         187         836
temp=68.2'C
frequency(48)=1200000000
throttled=0x50000

(Lousy power cable to Pi)
```


