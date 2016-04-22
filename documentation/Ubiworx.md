# Ubiworx

## What is Ubiworx?
>Ubiworx™ is our IoT software framework for embedded systems running Linux.
>Ubiworx enables embedded systems to bridge sensors, actuators and machines with data analytics systems and smart phone applications to form complete IoT Gateways in Internet of Things solutions.
>Ubiworx runs on Linux. We provide ubilinux, a Debian based Linux distribution, for Intel based maker boards.

## Prerequisites
>Before installing Ubiworx Lite on Intel Edison you will need the following:
>* Intel Edison Board
>Arduino Breakout Board
>USB Serial Connection Cable
>Power Supply or Another USB Cable
>Preinstall Ubilinux on the Intel Edison Board
>Connect the Intel Edison WiFi to the internet
>Linux installed on your computer

## Ubilinux

>Ubilinux is a Debian variant and allows installation onto the internal flash of an Intel Edison platform.
>We must have Ubilinux running and setup on the Intel Edison

##Considerations
>Now, the register function of Ubiworx is offline, so we cannot register, but this tutorial will serve as a guide.

## Set up
>We need to have an account for a ubiworx Broker.
>Go to http://www.ubiworx.com/ubiworx/ and click on the Download Ubiworks button, enter our information to register to get Ubiworx lite.
>Maker on the main menu. Then click on the Get ubiworx here button as shown below.
###Add a new Gateway
>To add a new gateway, go to the home view by clicking in the ubiworx logo or the home icon or visit https://broker.ubiworx.com/login/.
>In the gateway side navigation click on the Add button under the Configuration section.
>Fill in the form (not all fields are mandatory). See the section bellow with details about each field.
>>These mandatory fields can be filled up this way.
>>Name * 	Insert a name for the new gateway.
>>Unique ID * 	Insert a unique ID, this ID needs to be globally unique to your account. Note: this field can NOT be changed once created.
>>MAC * 	Identifies the hardware device being used. If a gateway needs to be replaced, the value in this field can be updated to reflect the new hardware.
>>The MAC address is inside the Edison, once logged in in the Edison type "ifconfig", under the wlan0 interface, there is a field called HWaddr along with some kind of hexadecimal number, this number without the ":" is the MAC address.
>Save changes using the button, the changes are saved on the ubiworx broker and will be synced when the gateway connects.
>You should be able to see your newly created Gateway in the dashboard.
>Note your vendor ID and your gateway ID for later use. Your vendor ID can be found by clicking on your username in the upper right corner. For viewing the gateway ID, go back to the dashboard and lookup its ID in the ID column.
###Edison 
>Now, connect to the Edison terminal and download the apt authentication key from the official ubiworx server by executing
>>"All the steps to connect to the Edison until we have root access"
>>We can have root access with the "su" command and the default password if Ubilinux is out of the box.
>>wget http://ubiworx.com/gpg.key -O - | apt-key add -
>Add the official ubiworx package repository to your sources.list.
>>echo "deb http://ubiworx.com/debian wheezy non-free" >> /etc/apt/sources.list
>Update your package index.
>>apt-get update
>Install ubiworx using apt-get. During the installation you will be asked for your vendor ID and gateway ID (device ID). Enter your notes from Add a new gateway.
>>apt-get install ubiworx-lite
>Start ubiworx and see your gateway going green on the webinterface.
>>/etc/init.d/ubiworx start




#References
http://www.ubiworx.com/ubiworx/help/documentation/gateway-install-guide/03-Edison.html
http://www.emutexlabs.com/ubilinux/29-ubilinux/218-ubilinux-installation-instructions-for-intel-edison
http://www.ubiworx.com/ubiworx/video-tutorials/getting-started/install-ubiworx-lite-on-intel-edison
http://www.emutexlabs.com/ubilinux/29-ubilinux/218-ubilinux-installation-instructions-for-intel-edison
https://learn.sparkfun.com/tutorials/loading-debian-ubilinux-on-the-edison