 BIOS:
In Security, disable Secure Boot.

Install yay to install packages from AUR

sudo pacman -S yay

Install an UI for tlp 
  yay -S tlpui
  

Install powertop
  yay -S powertop
  
  
Audio power saving
To shut down the audio card after 1 second of inactivity, add the following line in /etc/modprobe.d/audio_powersave.conf:

  options snd_hda_intel power_save=1
  
Applications

Chromium with vaapi (video acceleration) support:

  yay -S chromium-vaapi-bin
  
  
Insync (google drive client):
  yay -S insync insync-nautilus
  
Vmware Workstation (last version):
  yay -S vmware-workstation
  yay -S vmware-patch  

$ touch /tmp/x
$ sudo vmware-networks --migrate-network-settings /tmp/x

**** networking
++disable services

