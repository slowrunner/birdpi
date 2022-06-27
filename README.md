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



