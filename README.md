<div align='center'>
<img src="img/nethunter.png" alt="kali-nethunter" height="300"> <br>
  
# KALI NETHUNTER <br>
  
<img src="https://img.shields.io/badge/Android-green?style=flat&logo=Android&logoColor=white">
<img src="https://img.shields.io/badge/Red%20Team-red?style=flat&logo=amp&logoColor=white">
<img src="https://img.shields.io/badge/Blue%20Team-blue?style=flat&logo=bitwarden&logoColor=white">
<a href="https://github.com/thehackingsage"><img src="https://img.shields.io/badge/Mr.SAGE-11c28a?style=flat&logo=Github&logoColor=white"></a>
<br><br>
</div>

<div align='center'><img src="img/kali-nethunter.png" alt="Kali Nethunter"></div>

# Kali Nethunter :

Kali NetHunter is a free & Open-source Mobile Penetration Testing Platform for Android devices, based on Kali Linux. read more about nethunter here : https://www.kali.org/docs/nethunter/

Nethunter for Supported Devices : https://www.kali.org/get-kali/#kali-mobile

Nethunter for Unrooted Devices : https://www.kali.org/docs/nethunter/nethunter-rootless/

Nethunter for Rooted/Non-Supported Devices : https://www.kali.org/docs/nethunter/porting-nethunter/

# Nethunter for OnePlus3T

> ℹ️ For OnePlus3T Oxygen OS 9.0.6 Android 9 Pie

<div align='center'><img src="img/oneplus3t.png" alt="OnePlus3T Oxygen OS 9.0.6 Android 9 Pie"></div>

## Required Files :

- [x] [Fastboot and ADB](https://developer.android.com/studio/releases/platform-tools)
- [x] [OnePlus3T Driver](https://oneplususbdrivers.com/oneplus-3t-usb-driver-download/)
- [x] [TWRP for OnePlus3T](https://dl.twrp.me/oneplus3/twrp-3.5.2_9-0-oneplus3.img.html)
- [x] [Magisk v23.0](https://magiskapp.com/zip/#download-now)
- [x] [OnePlus3T Oxygen OS 9.0.6](https://otafsg1.h2os.com/patch/amazone2/GLO/OnePlus3TOxygen/OnePlus3TOxygen_28.A.86_GLO_086_1911042121/OnePlus3TOxygen_28_OTA_086_all_1911042121_9156030ead54e.zip) (Stock Rom) (Android 9.0)
- [x] [Kali Nethunter for OnePlus3T](https://kali.download/nethunter-images/kali-2021.3/nethunter-2021.3-oneplus3-any-pie-kalifs-full.zip)
- [x] [Boot Patched 9.0.6 OnePlus3T](https://drive.google.com/file/d/1fffJ551Trf4TY1WsEUDPj5vhEn_1F9zt/view?usp=sharing)
- [x] [Force_Encryption_Disabler_For_OOS_Pie_v1](https://drive.google.com/file/d/1WamN3fZjkadPXc3y2SK0yFLrupP72H9v/view?usp=sharing)
- [x] Type-C OTG Cable ([Amazon India](https://www.amazon.in/s?k=type-c+otg+cable))
- [x] USB Flash Drive ([Amazon India](https://www.amazon.in/s?k=usb+stick))
- [x] C-Type USB Cable

### ℹ️ BACKUP ALL YOUR DATA BEFORE DOING ANYTHING.

## Unlock OnePlus3T Bootloader :

- Enable Developer Option : Go to `Settings > About Phone > Tap on Build Number 7 times`.
- Go to `Settings > System > Developer Options`
- Enable USB Debugging Mode, OEM Unlocking and Advanced Reboot

<div align='center'><img src="img/enable-developer-option.png" alt="Enable Developer Option"></div>

<div align='center'><img src="img/developer-option.png" alt="Enable USB Debugging Mode, OEM Unlocking and Advanced Reboot"></div>

> ⚠️ *Unlocking Bootloader will completely reset your phone to factory defaults! Backup all your data before doing this.*

- Boot OnePlus3T into fastboot mode by long pressing the power button and then select `Bootloader` Option, or you can also boot your device into fastboot mode by turning off the device then long pressing volume up + power button.
- After that connect your device to PC via USB cable.
- Extract Fastboot and ADB (platform-tools_rxx.x.x-windows.zip) 
- Open the Terminal in the extracted Fastboot and ADB folder by pressing `Shift + Right Click > Windows Terminal`

<div align='center'><img src="img/fastboot-and-adb.png" alt="Fastboot and ADB" height="500"></div>

- Verify the device’s connection by executing the following command :

```
fastboot devices
```

<div align='center'><img src="img/fastboot-devices.png" alt="Fastboot Devices" height="500"></div>

- Now, unlock the bootloader by typing the following command :

```
fastboot oem unlock
```

<div align='center'><img src="img/fastboot-oem-unlock.png" alt="Fastboot OEM Unlock" height="500"></div>

- You will get finished output in the terminal and phone will reboot, let it boot completly and setup your android device.

## Flash TWRP Recovery :

- After Unlocking Bootloader, reboot and setup your android.
- Again, Enable Developer Option.
- Enable USB Debugging Mode, OEM Unlocking and Advanced Reboot. 
- Reboot OnePlus3T into fastboot mode and connect your device to PC via USB cable.
- Move TWRP img file to the extracted Fastboot and ADB folder

> ⚠️ *You can also change the TWRP img file name to `twrp.img` with the actual filename. just for shorten the command.* 😅

<div align='center'><img src="img/fastboot-twrp.png" alt="Fastboot TWRP" height="500"></div>

- Open the Terminal by pressing `Shift + Right Click > Windows Terminal`

- Verify the device’s connection by executing the following command :

```
fastboot devices
```

<div align='center'><img src="img/fastboot-devices.png" alt="Fastboot Devices" height="500"></div>

- Now, Flash TWRP Recovery by executing the following command :

```
fastboot flash recovery twrp.img
```

<div align='center'><img src="img/flash-recovery.png" alt="Flash Recovery" height="500"></div>

- That's it !!! You have successfully installed TWRP Recovery.
- Now, navigate to TWRP Recovery with your volume keys and select it with the power button.

> ⚠️ *You can also create a backup using TWRP and move it to your PC or USB Stick so if anything goes wrong you can restore your stock android*

## Wipe All Data and Flash Stock Rom and Patches :

- Reboot to TWRP Recovery

<div align='center'><img src="img/twrp-recovery.png" alt="TWRP Recovery" height="500"></div>

- Format DALVIK, SYSTEM, CACHE : `Wipe > Swipe to Factory Reset`
1
<div align='center'><img src="img/factory-reset.png" alt="Factory Reset" height="500"></div>

- Don't Reboot !!

- Copy all files to the USB Stick :
	+ OnePlus3TOxygen_28_OTA_086_all_1911042121_9156030ead54e.zip
	+ boot-patched-9.0.6-OP3T.img
	+ Force_Encryption_Disabler_For_OOS_Pie_v1.zip
	+ Magisk-v23.0.zip 
	+ nethunter-2021.3-oneplus3-any-pie-kalifs-full.zip

- Connect The USB Stick with Android Device using OTG Cable.
- Mount OTG by going to `Mount > Select USB-OTG Partition`
- Select Storage USB-OTG by going to `Mount > Select Storage > Select USB-OTG`

<div align='center'><img src="img/usb-otg.png" alt="USB-OTG" height="500"></div>

- Flash OnePlus3T Stock Rom : `Install > Select OnePlus3TOxygen_28_OTA_086_all_1911042121_9156030ead54e.zip file > Swipe to Install`

<div align='center'><img src="img/oneplus3t-rom.png" alt="OnePlus3T Stock Rom" height="500"></div>

- Don't Reboot !!
- Flash boot-patched-9.0.6-OP3T.img : `Install > Install Image > Select boot-patched-9.0.6-OP3T.img file > Swipe to Install`

<div align='center'><img src="img/boot-patched.png" alt="Boot Patched" height="500"></div>

> ⚠️ *Flash boot-patched-9.0.6-OP3T.img to disable DM-Verity*

- Go back and Flash Force_Encryption_Disabler_For_OOS_Pie_v1.zip : `Install > Select Force_Encryption_Disabler_For_OOS_Pie_v1.zip file > Swipe to Install`

<div align='center'><img src="img/force-encryption-disabler.png" alt="Force Encryption Disabler For OOS Pie v1" height="500"></div>

- Again go back and Flash Magisk-v23.0.zip : `Install > Select Magisk-v23.0.zip > Swipe to Install`

<div align='center'><img src="img/magisk.png" alt="Magisk" height="500"></div>

- After installing make sure to wipe cache/dalvik

- Now reboot to system and setup your android device.!!

## Install Kali Nethunter :

- Once you setup your device again reboot to Recovery.
- Go To `Advance > Terminal`

- Type `df system -h` and look at the free space in system partition, make sure you have atleast 100MB free space.

<div align='center'><img src="img/terminal.png" alt="Terminal" height="500"></div>

- If you don't have enough free space then mount system in TWRP : `Mount > Select System`
- Go to `File Manager > System > Apps` and free some space by deleting some unwanted apps like play games, play movies, youtube, duo etc. (Beware : Don't Delete System Apps)

> ⚠️ *If there is low space on your system partition that fstab file flashing fails resulting in blank fstab file and you will end up in bootloop.*

- Then check again the free space from terminal, Once you have confirmed that you have atleast 100MB of free space left in system partition follow the next step
- Now Flash nethunter-2021.3-oneplus3-any-pie-kalifs-full.zip : `Install > Select nethunter-2021.3-oneplus3-any-pie-kalifs-full.zip > Swipe to Install`

<div align='center'><img src="img/oneplus3t-nethunter.png" alt="NetHunter on OnePlus3T" height="500"></div>

- This process can take up to 25 minutes so keep patience.

<div align='center'><img src="img/nethunter-log.png" alt="NetHunter on OnePlus3T" height="500"></div>

- Once the flash is successful, Flash Magisk-v23.0.zip Again : `Install > Select Magisk-v23.0.zip > Swipe to Install` 

<div align='center'><img src="img/magisk.png" alt="Magisk" height="500"></div>

- After installing make sure to wipe cache/dalvik

- That's It. Reboot Your Device.

<div align='center'><img src="img/nethunter-home.png" alt="Kali NetHunter on OnePlus3T" height="500"></div>

## Things To Do After Installation :

- Update NetHunter App after flashing.
- Open the NetHunter App and start the Kali Chroot Manager.
- Install the Hacker Keyboard from the NetHunter Store using the NetHunter Store app.
- Install any other apps from the NetHunter Store as required.
- Set up Nethunter KeX.
- Configure Kali Services, such as SSH.
- Set up custom commands.
- Initialize the Exploit-Database.
- If you want you can also Add Metapackage.
- Open Nethunter Terminal and Update and Upgrade Kali.

<div align='center'><img src="img/kali-chroot.png" alt="Kali Chroot" height="500"></div>

That's it !!! if you face any issue feel free to ask..

## Source : 

- XDA-Forum : https://forum.xda-developers.com/t/disable-dm-verity-force-encryption-oneplus-3t-3-for-pie-oxygen-os.3922324/
- Kali Nethunter : https://www.kali.org/docs/nethunter/

**Happy Hunting !!!**
