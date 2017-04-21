# win-usb-resset

#### A script for rebooting the USB device.


**Compatible:** Windows 7 and higher

**Architecture:** х64

**Package Contents:** 
* devcon.exe (64) - Device Console, is a command-line tool that displays detailed information about devices on computers running Windows
* devcon-remove-rescan.bat - USB device reset script

### Notes:
To determine the device ID, execute the following command in the CMD:
```
C:\>devcon.exe status USB*
```

**You will get the following output**
```
C:\>devcon.exe status USB*
USB\VID_1410&PID_9020\0123456789ABCDEF
    Name: MiFi USB620L
    Driver is running.
USB\ROOT_HUB\4&211F7785&0
    Name: USB Root Hub
    Driver is running.
USB\ROOT_HUB\4&281C4CA4&0
    Name: USB Root Hub
    Driver is running.
USB\ROOT_HUB\4&35CF8E68&0
    Name: USB Root Hub
    Driver is running.
USB\ROOT_HUB\4&484FDEF&0
    Name: USB Root Hub
    Driver is running.
USB\ROOT_HUB20\4&244E1552&0
    Name: USB Root Hub
    Driver is running.
USB\ROOT_HUB20\4&35568869&0
    Name: USB Root Hub
    Driver is running.
USB\ROOT_HUB\4&10EA4A84&0
    Name: USB Root Hub
    Driver is running.
USB\ROOT_HUB\4&1F0CB10&0
    Name: USB Root Hub
    Driver is running.
9 matching device(s) found.                                                                                                                                                                                                                                                                                                                                                                                                                                                    
```

In my case, the device ID is **VID_1410**

The line ```timeout /t 30 /nobreak>nul``` specifies the delay interval between execution of script commands. In this case, the delay is 30 seconds.

