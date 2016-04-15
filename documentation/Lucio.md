# Lucio

Introduction:

In Arduino environment, it's convenient to access BT SPP like a serial port and react to the command string sent from the BT serial port. Many Arduino projects have utilized this way to allow remote control for their projects. In the past, you'll need additional BT shield or BT kit to archive it on Intel® Galileo. Now, since we have built-in BT support on Intel® Edison, you can use Edison module with Arduino breakout board to do it. NO additional BT shield is required!

![Arch](https://software.intel.com/sites/default/files/managed/d7/64/SystemArch4.png)

System Architecture

Requirements:

An Android* phone or tablet running Android and has Bluetooth.

Connect your Intel® Edison board to a Wi-Fi* network, see Get started with Intel® Edison technology. Specified a name for your Edison, for ex: myedison.

SCP using a host computer connected to the same network

Establish a terminal to your board either Via Serial port or SSH.

Background:

Connecting the Intel® Edison board to your Android* Phone with Serial Port Profile (SPP) describes how to connect your Edison board to Android* Phone with SPP, however, you cannot get the input from SPP in your Arduino code. In Connecting to Intel® Edison from Android* with Bluetooth* LE (BLE) describes a way to access BT via Arduino code but additional BT shield/kit is required.

Since we have built-in BT, why don't we just take the advantage of it? Here I provide an example library to do that.

One efficient way to communicate between Arduino and Linux in Intel® Edison is to use mmap(). See Efficient communication between Arduino* and Linux native processes. However, it's not easy to use the in-memory shared lock between python process and Arduino process.

So I choose named pipe as a simple way to implement IPC between Arduino sketch process and BT SPP python service process.

Setup for Edison Bluetooth service:

1. Download the file bluetooth-service.tar.gz

2. Copy bluetooth-service.tar.gz to /home/root/Bluetooth and extract it

1
mkdir /home/root/bluetooth
2
cd /home/root/bluetooth
3
mv /home/root/bluetooth-service.tar.gz ./
4
tar -xvf bluetooth-service.tar.gz
3. Copy bluetooth-spp-pin.service to /lib/systemd/system/

1
cp bluetooth-spp-pin.service /lib/systemd/system
4. Enable the systemd service

1
systemctl enable bluetooth-spp-pin
5. Reboot your device

1
reboot
6. Double check the service

1
systemctl status bluetooth-spp-pin
 

Setup for Edison Arduino sketch:

1. Download the library Intel-Edison-BT-SPP-Library.zip.

2. Extract to your Arduino library path, ex: C:\Users\username\Documents\Arduino\libraries, check it in your Arduino IDE, File->Preferences->Sketchbook Location

3. Restart your Intel® Arduino IDE v1.6.0 or later version

4. Open the example bt_test under File->Examples->Intel Edison BT SPP Driver Library

5. Verify and Upload the sketch to your Edison

6. Open Serial Monitor so we can check the output after we send something to it.

 

Setup for your Phone:

1. Download and install any BT SPP APP from PlayStore. For ex: BLE_SPP_PRO.

2. Turn on BT on your phone and connect to your Edison module

3. Enter the PIN code, the default PIN is 8888, feel free the change it later at line 70 of bluetooth-pin-service.py

4. Connect to your Edison in the APP, for ex: myedison

5. Send something to your Edison, you should be able to see the result on Serial Monitor of Arduino IDE

![CMD](https://software.intel.com/sites/default/files/managed/a1/07/BLE_SPP_PRO%20-%20Copy.png)

Sent a string from BT SPP APP

Recevied text via BT SPP

Conclusion:

Now you have a fixed PIN BT device which support SPP. So you can connect to it very easily just like you connect to your BT speaker. The BT works after boot automatically, and you don’t need to pair the device via terminal. You can access BT SPP in your Arduino code, treat it as a serial device and connect to your Edison project via Android phone with BT SPP App. This means you can control your Edison projects remotely to do whatever you want. Base on this work, you can develop a lot of interesting applications with build-in BT function of Intel® Edison. Have fun and do share your projects with us!