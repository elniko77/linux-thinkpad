
### BIOS:

 In Security, disable Secure Boot.

Install yay to install packages from AUR (yaourt is deprecated):

    sudo pacman -S yay
    

Install Power utils:

    <code> yay -S tlpui powertop </code>
  

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

### Virtualization

For install vmware workstation must install dkms first
 yay -S dkms vmware-workstation

Vmware gives an error the first time, because the networking file is missing. You have to create it.
 $ touch /tmp/x
 $ sudo vmware-networks --migrate-network-settings /tmp/x

 networking
disable services

### Fingerprint reader

The x270 and t470 models have the Validity VFS0090 fingerprint reader. It's not supported in the current version of libfprint library, so you must install the patched version:

  yay -S libfprint-vfs0097-git 

### Development

 yay -S code

Vscode plugins: docker, Markdown All in One, powershell, python, remote Containers, remote ssh , remote wsl, remote development

### Terminal

Install oh my zsh!
 
  `sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
  
Clone my repo for tmux, vim and zsh:

 `git clone https://github.com/elniko77/dotfiles.git
 
  sh ./dotfiles/bootstrap.sh`
  
  



