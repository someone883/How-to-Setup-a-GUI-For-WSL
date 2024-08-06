## How-to-Setup-a-GUI-For-WSL
WARNING!

I will **NOT** be showing you how to install WSL or Ubuntu so please install before reading this

**1.** *sudo apt-get update -y && sudo apt-get upgrade -y*

**2.** *lsb_release -a* ubuntu version should be 22.04 or above

**3.** *sudo apt install -y xfce4*

**4.** *sudo apt install xfce-goodies*

**5.** *sudo cp /etc/xrdp/xrdp.ini /etc/xrdp/xrdp.ini.bak*

**6.** *sudo sed -i 's/3389/3390/g' /etc/xrdp/xrdp.ini'

**6.** *sudo sed -i 's/max_bpp=32/#max_bpp=32\nmax_bpp=128/g' /etc/xrdp/xrdp.ini*

**6.** *sudo sed -i 's/xserverbpp=24/#xserverbpp=24\nxserverbpp=128/g' /etc/xrdp/xrdp.ini*

**7.** *echo xfce4-session > ~/.xsession

**8.** *sudo nano /etc/xrdp/startwm.sh*

**9.** comment last 2 lines then type in *startxfce4* then Ctrl S and Ctrl X

**10.** *sudo /etc/init.d/xrdp start*

**11.** open Remote Desktop Configuration and type in *localhost:3390*

And You're done!
