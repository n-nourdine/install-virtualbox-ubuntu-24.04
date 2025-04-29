# install-virtualbox-ubuntu
## Step 1: Add the following line to your /etc/apt/sources.list. For Ubuntu 22.04 and older, 'replace '<mydist>' with 'jammy', 'eoan', 'bionic', 'xenial',

deb [arch=amd64 signed-by=/usr/share/keyrings/oracle-virtualbox-2016.gpg] https://download.virtualbox.org/virtualbox/debian <mydist> contrib

## Step 2: Ensure VirtualBox and DKMS Are Properly Installed
### Remove any broken installations:

bash ```
sudo apt remove --purge virtualbox virtualbox-dkms
sudo rm -rf /usr/src/vboxhost-*

### Reinstall VirtualBox and DKMS:

sudo apt update
sudo apt install virtualbox virtualbox-dkms

### Install Linux headers (required for DKMS):
sudo apt install linux-headers-$(uname -r)
```
