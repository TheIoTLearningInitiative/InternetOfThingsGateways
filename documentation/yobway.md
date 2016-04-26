# YoBWay

## What is it?
>Yocto Basic Gateway is a project based on Yocto, Intel Edison and some connectivity protocols.

## Prerequisites
>You must have an Intel Edison up running without any troubles and connected via serial connection.
>Make sure you have the latest Intel Edison Yocto image installed.
>>you can check version ```cat /etc/version``` or ```configure_edison --version```

## Setup
>Now run configure_edison --setup, the option --setup is not present before doing an successful upgrade always check for latest image updates: configure_edison --upgrade 

>Hint: if you are on build >=68 you can activate the Wifi AP mode (see section down) and run the configuration via webconsole http://your_Edison_IP_address

### Turning Edison into an WLAN/WiFi Accesspoint
>working as well just press the power button between 4sec & 7sec sec and you will
find a hotspot with the name you have given your Edison during setup, use the given root pwd
to get a connection. My Edison can now be reached e.g. from smartphone via SSH your_Edison_IP_address
(notice different network setting as with DHCP above) ATTENTION: will stay in AP mode after reboot!

You want manuelly to switch back from AP mode in Client mode of Wifi? simply run configure_edison –setup again

systemctl stop hostapd
systemctl disable hostapd
systemctl enable wpa_supplicant
systemctl start wpa_supplicant
wpa_cli reconfigure
wpa_cli select_network wlan0
udhcpc -i wlan0


### Turning Edison into an Beacon/iBeacon:
>Remembering what is a Beacon
>rfkill unblock bluetooth
hciconfig hci0 up
hcitool lescan
LE Scan …
63:58:79:E0:17:7C (unknown) In this example an Estimote Beacon was found!
63:58:79:E0:17:7C (unknown)
Ctrl+C Stop Scan

OK Bluetooth Low Energy based on blueZ (5.18) is up and running!







