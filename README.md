# bluetooth
Bluetooth based projects<br>
I did not write this application, it was provided by "Nordic Semiconductor", I just adjusted the eclipse project setting for BLE400 board by "Waveshare".<br>
 I was frustrated when I coud not find any proper setup for using the nRF5 SDK for nRF51822 with eclipse and gcc. The command line interface provided by them works great, but wanted to use on eclipse. After some time I got it working for waveshare board.<br>
 This project thus I pushed here to have backup and to get started the setup for these devices. Nordic Semiconductor, I think  they are focusing on new nRF52 chips, they may have removed support for this IC in their new SDK releases.<br>
 <br>
Based on nRF51822 <br>
SDK used nRF5 version 12.3.0, (bacause this could be last sdk for nRF51 using softdeice S130) <br>
Official download: https://www.nordicsemi.com/Software-and-tools/Software/nRF5-SDK/Download <br>
<br>
Softdevice: S130 latest <br>
GCC Toolchain used: gcc-arm-none-eabi-9-2019-q4<br>
Eclipse environment: Eclipse IDE for C/C++ Developers, Version: 2020-03 (4.15.0), Build id: 20200313-1211<br>
<br><br>
Usage:<br>
First flash the softdevice hex, then blinky.hex and reset the device.<br>
OR you can merge the sofdevice hex with blinky.hex using mergehex command line tools provided by Nordic Semiconductor.<br>
Then flash it using JLink or similar programming tool.<br>
