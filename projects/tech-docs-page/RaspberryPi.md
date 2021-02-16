# Install on Raspberry Pi
## Why a Raspberry Pi?

Raspberry Pi is an inexpensive computing hardware platform 
that generates little heat, draws little power, 
and can run silently 24 hours a day without having to think about it.

## Steps to Follow
1. __Prepare the MicroSD Card__
The MicroSD card will likely come formatted as exfat, instead of FAT32, but the Raspberry Pi needs FAT32. 
I recommend using the built-in tools on Windows or Mac OS X to format the MicroSD.  
If you only have a Linux box to start, you probably already know how to format the microSD card. 

2. __Install the operating system__ 
Installing software on a Raspberry Pi can be mildly complicated.   
I suggest using their [NOOBS install manager](https://www.raspberrypi.org/documentation/installation/noobs.md) to make it painless. 
Just follow the link for [NOOBS](https://www.raspberrypi.org/documentation/installation/noobs.md), download the files and copy them to your FAT32 microSD card and get ready to turning things on.

3. __Initial configuration__ 
There are ways to avoid using a keyboard, video display, and mouse (KVM) altogether.  
But in the interest of keeping things simple, I recommend putting your Raspberry Pi into its case, then insert the microSD card into your Raspberry Pi, hook up the KVM cables, plugin the ethernet cable, and plugin the power.   
At boot up, select Raspbian as your operating system and let NOOBS get the OS set up. Do not bother with any setting that will launch “startx” (the GUI interface) at boot time, since this full node will only be configured via command line.  

4. __Update Raspberry Pi__
Add “en_US.UTF-8 UTF-8” to the locale list and set your time zone and then reboot:
```
    sudo raspi-config
    sudo reboot
```
Keep everything fresh:
```
    sudo apt-get update
    sudo apt-get upgrade
```
Install dependencies (broken up here to show more cleanly – you can do one apt-get call if you want):
```
    sudo apt-get install build-essential autoconf libssl-dev libboost-dev 
    sudo apt-get install libboost-chrono-dev libboost-filesystem-dev
    sudo apt-get install libboost-program-options-dev libboost-system-dev 
    sudo apt-get install libboost-test-dev libboost-thread-dev libtool
```
Prepare for and download bitcoin source code:
```
    mkdir ~/bin
    cd ~/bin
    git clone -b v0.11.2 https://github.com/bitcoin/bitcoin.git
    cd bitcoin/
```

Configure and compile the source code; install to the bin directory (this will take 30+ minutes):
```
    ./autogen.sh
    ./configure CPPFLAGS="-I/usr/local/BerkeleyDB.4.8/include -O2" LDFLAGS="-L/usr/local/BerkeleyDB.4.8/lib" --disable-wallet
    make
    sudo make install
```

5. __Verify your Bitcoin full node is working__ 
Assuming all went well (above) you can just type the following in your command line:
```
    bitcoind &
```
The & at the end tells the app to run in the background so that your command line interface can be used for more commands. If you type the following you will see the status of your Bitcoin full node:
```
    bitcoin-cli getinfo
```

It will likely tell you that it is loading the blockchain or tell you how many blocks have been loaded thus far. If you made it this far, congratulations! Unfortunately, you are far from over. For now, just stop the Bitcoin server you just worked so hard to start with the following command:
```
    bitcoin-cli stop
```

6. __Side-load the blockchain__  
Synchronize the blockchain on your primary machine and then simply copy your personal seed of the Bitcoin blockchain to your Raspberry Pi full node. The files you need are in the ‘blocks’ folder and the ‘chainstate’ folder. You can use the following command using SCP (basically SSH for copying files) to move the files from your main computer to your Raspberry Pi full node (you can also use WinSCP on a Windows machine or Cyberduck on a Mac – but I prefer the command line):
```
    scp -r blocks your_username@raspberrypiIPaddress:/home/pi/.bitcoin
    scp -r chainstate your_username@raspberrypiIPaddress:/home/pi/.bitcoin
```
Now you should be able to start up your bitcoin server again and start relaying Bitcoin transactions in realtime. Just execute the Bitcoin server command:
```
    bitcoind &
```
7. __Turn on port forwarding in your router__ 
You need to enable port forwarding on your router to point to port 8333 to your internal Bitcoin full node IP address.  
I’m not sure if you need both TCP and UDP forwarded, but I did both and everything is working great.  
_How do you do this?_ Each router is different and each cable/fiber/DSL provider has instructions somewhere. Your router, in fact, might automatically do it for you, since gaming machines like the XBOX and Playstation benefit from port forwarding and ISPs don’t want to deal with explaining how to set it up, so they auto-detect services you are running that need port forwarding and make it happen.  
_Why do you need port forwarding?_ Basically it allows other Bitcoin peers to automatically connect to you without the need for you to invite them first. Without port forwarding you will have far fewer peers and not allow the Bitcoin network to be healthy. 
So much so, that you cannot really claim you are running a full node without port forwarding (or wide open IP access) enabled.

8. __Run & Check__
You should be all set! Remember when you want to check in on things just open and SSH connection and run:
```
    bitcoin-cli getinfo
```

## Sources
__Raspberrypifullnode__ by [David Carns](https://github.com/Dcarns) [https://www.raspberrypifullnode.com/](https://www.raspberrypifullnode.com/)

