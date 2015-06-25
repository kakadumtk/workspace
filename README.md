**Q: Windows cannot detect the USB COM port of LinkIt ONE**

**A:** Make sure the [Windows USB COM Port Driver](http://download.labs.mediatek.com/mediatek_linkit_windows-com-port-driver.zip) is installed, and the MS <-> UART switch is in UART mode. Then plug in the LinkIt ONE board.
	If you see an "Alcatel RNDIS" device appears and disappears in the Device Manager when connecting and disconnecting LinkIt ONE, uninstall the COM port driver, launch "device installation settings" in "advanced system window", and choose "Never install driver software from Windows update". Then re-install the COM port drivers and plug in the LinkIt ONE board.

![Device Installation Settings](https://cloud.githubusercontent.com/assets/10078694/8348407/f06bd960-1ac7-11e5-9a89-9895bcbdde04.PNG)

**Q: The COM ports appear and disappear when connecting or resetting the board**

**A:** The USB COM ports on LinkIt ONE is emulated by the system-on-chip itself. So when the chip is reset, e.g. after uploading sketches, the COM ports will disappear and reappear.

**Q: Firmware Updater fails to detect the board**

**A:** Make sure you have installed USB COM port driver of LinkIt ONE. Prior the firmware update, make sure the MS <-> UART switch is in MS mode. If the switch is in UART mode, the firmware updater will report a timeout error.

**Q: OS X cannot detect the USB COM port of LinkIt ONE**

**A:** On OS X, make sure you have updated the firmware later than 1.1.08 of the LinkIt ONE, and make sure you have installed the [OS X COM Port Driver](http://download.labs.mediatek.com/mediatek_linkit_os-x-com-port-driver.zip) prior to updating the firmware.

**Q: My SIM card does not work**

**A:** LinkIt ONE supports only GSM and GPRS(2.5G). 3G-only SIM cards are not supported. To connect to GPRS, make sure the APN and user name settings are correct.

**Q: The board keeps resetting itself**

**A:** Make sure the USB <-> BAT switch is in the USB position if there is no battery connected. If you switch to BAT (for Battery) mode, without attaching a battery, the board will keep resetting itself.
