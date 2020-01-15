
#### BIOS:

  In Security, disable Secure Boot.

#### Package management:


  Install yay to install packages from AUR (yaourt is deprecated):

  ```console
    $ sudo pacman -S yay
  ```
    
#### Power Management:

  Install Power utils (tlp is already installed):

  ```console
    $ yay -S tlpui powertop
  ```
  
  Audio power saving
  To shut down the audio card after 1 second of inactivity, add the following line in /etc/modprobe.d/audio_powersave.conf:

    options snd_hda_intel power_save=1
  
#### Install commmon apps:

  Chromium with vaapi (video acceleration) support:

  ```console
    $ yay -S chromium-vaapi-bin
  ```

  Insync (google drive client):

  ```console  
    $ yay -S insync insync-nautilus
  ```
  Tools:
  
  ```console
    $ yay -S freerdp remmina vlc wireguard-tools
  ```

#### Virtualization

  For install vmware workstation must install dkms first
 
  ```console
    $ yay -S dkms vmware-workstation
  ```
  
  Vmware gives an error the first time, because the networking file is missing. You have to create it.
 
  ```console
    $ touch /tmp/x
    $ sudo vmware-networks --migrate-network-settings /tmp/x
  ```

#### Fingerprint reader

The x270 and t470 models have the Validity VFS0090 fingerprint reader. It's not supported in the current version of libfprint library, so you must install the patched version:

```console
    $ yay -S libfprint-vfs0097-git 
```

#### Development

 Install visual studio code
 
 ```console
    $ yay -S code
 ```
 Vscode plugins: docker, Markdown All in One, powershell, python, remote Containers, remote ssh , remote wsl, remote development

#### Terminal

Install oh my zsh! (first install powerline for agnoster theme)
 
 ```console
  $ yay -S powerline-fonts
  $ sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

Clone my repo for tmux, vim and zsh (personal dotfiles configs):

```console
  $ git clone https://github.com/elniko77/dotfiles.git
  $ sh ./dotfiles/bootstrap.sh
```


  
  



