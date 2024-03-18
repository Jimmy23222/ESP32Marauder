# JLCPCB Firmware Upload Instructions
The following documentation describes the process for installing the ESP32 Marauder firmware on official supported hardware. The specific hardware detailed in the documentation is the ESP32 Marauder v6.1 and the ESP32 Marauder Mini. The process for installing the firmware is the same between the two devices. The only point that changes is the specific variation of the ESP32 Marauder firmware binary. As they have different hardware configurations, they both have their own version of the firmware. As such, I have written the documentation separately for both hardware versions but you will see the process is the same apart from the specific bin selection.

## Boards
- [ESP32 Marauder v6.1](#esp32-marauder-v61)
- [ESP32 Marauder Mini](#esp32-marauder-mini)

## ESP32 Marauder v6.1
![4F1A9182-FA9D-4B22-91D1-280A81FD77AB - Copy](https://github.com/justcallmekoko/ESP32Marauder/assets/25190487/8824ef6d-5574-490c-b3de-ea900a4edd8f)

1. Download the firmware files required for the ESP32 Marauder v6.1
    - [Bootloader](https://github.com/justcallmekoko/ESP32Marauder/raw/master/FlashFiles/MarauderV4/esp32_marauder.ino.bootloader.bin)
    - [Partitions](https://github.com/justcallmekoko/ESP32Marauder/raw/master/FlashFiles/MarauderV4/esp32_marauder.ino.partitions.bin)
    - [Boot App](https://github.com/justcallmekoko/ESP32Marauder/raw/master/FlashFiles/FlipperZeroMultiBoardS3/boot_app0.bin)
    - The [latest release](https://github.com/justcallmekoko/ESP32Marauder/releases/latest) of the ESP32 Marauder firmware
        - **For this device, the firmware name schema is `esp32_marauder_vX_X_X_XXXXXXXX_v6_1.bin`**
2. Download, unzip, and open the [Espressif Flash Download Tool](https://github.com/justcallmekoko/ESP32Marauder/raw/master/FlashFiles/flash_download_tool_3.9.5.zip)
    - Chip Type: `ESP32`
    - Work Mode: `Factory`
3. Using a USB-C cable, connect the assembled PCB to the workstation you are using for firmware upload
    - **NOTE:** In `Factory` mode, up to eight PCBs can be connected and flashed at once  
![41235E60-7069-4747-A6C9-CDF10C912752 - Copy](https://github.com/justcallmekoko/ESP32Marauder/assets/25190487/7b637bc3-593e-4f30-932c-3e3099e71778)

4. Configure the Espressif Flash Download Tool for firmware upload
    - Download Path Config (using downloaded firmware files)
        - `esp32_marauder.ino.bootloader.bin` @ `0x1000`
        - `esp32_marauder.ino.partitions.bin` @ `0x8000`
        - `boot_app0.bin` @ `0xE000`
        - `esp32_marauder_vX_X_X_XXXXXXXX_v6_1.bin` @ `0x10000`
        - **MAKE SURE THOSE FOUR CHECK BOXES ARE CHECKED**
    - SPI Speed: `80MHz`
    - SPI Mode: `QIO`
    - DownloadPanel BAUD: `921600`
    - DownloadPanel COM:
        - Select the COM associated with the PCB's CP2102 chip. This can be done by locating the device in Device Manager
![image](https://github.com/justcallmekoko/ESP32Marauder/assets/25190487/6a555947-ec88-4827-b277-53119fd8be64)
    - Your Espressif Flash Download Tool window should now appear like the image below...
![image](https://github.com/justcallmekoko/ESP32Marauder/assets/25190487/c67e9e79-37db-42aa-aaa4-f0685dd17b19)

5. Click the `START ALL` button and allow the firmware to upload to the on-board ESP32 modules
6. Once the firmware installation completes and the DownloadPanel says `FINISH`, press the `RESET` button on the PCB  
![F18707AD-3E24-47BB-B2C2-14CA9295C846 - Copy](https://github.com/justcallmekoko/ESP32Marauder/assets/25190487/b1de1d25-fda6-40d2-81c1-5765fe62c1a3)


**THIS CONCLUDES THE FIRMWARE UPLOAD INSTRUCTIONS FOR THE ESP32 MARAUDER V6.1**
**PLEASE PROCEED TO [TESTING](#testing)**

## ESP32 Marauder Mini

![8F22CD8E-E77E-4A1F-992A-AB90D115028A - Copy](https://github.com/justcallmekoko/ESP32Marauder/assets/25190487/c8341735-0525-45a4-86f6-4ec2d8065bc3)

1. Download the firmware files required for the ESP32 Marauder Mini
    - [Bootloader](https://github.com/justcallmekoko/ESP32Marauder/raw/master/FlashFiles/MarauderV4/esp32_marauder.ino.bootloader.bin)
    - [Partitions](https://github.com/justcallmekoko/ESP32Marauder/raw/master/FlashFiles/MarauderV4/esp32_marauder.ino.partitions.bin)
    - [Boot App](https://github.com/justcallmekoko/ESP32Marauder/raw/master/FlashFiles/FlipperZeroMultiBoardS3/boot_app0.bin)
    - The [latest release](https://github.com/justcallmekoko/ESP32Marauder/releases/latest) of the ESP32 Marauder firmware
        - **For this device, the firmware name schema is `esp32_marauder_vX_X_X_XXXXXXXX_mini.bin`**
2. Download, unzip, and open the [Espressif Flash Download Tool](https://github.com/justcallmekoko/ESP32Marauder/raw/master/FlashFiles/flash_download_tool_3.9.5.zip)
    - Chip Type: `ESP32`
    - Work Mode: `Factory`
3. Using a USB-C cable, connect the assembled PCB to the workstation you are using for firmware upload
    - **NOTE:** In `Factory` mode, up to eight PCBs can be connected and flashed at once  
![3FD2E498-E6A2-4ABF-AFFB-9FD5BE04A1DF - Copy](https://github.com/justcallmekoko/ESP32Marauder/assets/25190487/8a88772c-d675-4103-b2f9-f628290ad890)

4. Configure the Espressif Flash Download Tool for firmware upload
    - Download Path Config (using downloaded firmware files)
        - `esp32_marauder.ino.bootloader.bin` @ `0x1000`
        - `esp32_marauder.ino.partitions.bin` @ `0x8000`
        - `boot_app0.bin` @ `0xE000`
        - `esp32_marauder_vX_X_X_XXXXXXXX_mini.bin` @ `0x10000`
        - **MAKE SURE THOSE FOUR CHECK BOXES ARE CHECKED**
    - SPI Speed: `80MHz`
    - SPI Mode: `QIO`
    - DownloadPanel BAUD: `921600`
    - DownloadPanel COM:
        - Select the COM associated with the PCB's CP2104 chip. This can be done by locating the device in Device Manager
![image](https://github.com/justcallmekoko/ESP32Marauder/assets/25190487/370df2ca-c3f8-495e-9e86-596c28f75f29)
    - Your Espressif Flash Download Tool window should now appear like the image below...
![image](https://github.com/justcallmekoko/ESP32Marauder/assets/25190487/1ba8b975-5d2e-4c5f-8cdb-ac29f7828d69)

5. Click the `START ALL` button and allow the firmware to upload to the on-board ESP32 modules
6. Once the firmware installation completes and the DownloadPanel says `FINISH`, press the `RESET` button on the PCB  
![EC59D0C5-D268-4AC4-9B4C-75A73278E835 - Copy](https://github.com/justcallmekoko/ESP32Marauder/assets/25190487/f878991e-27a7-4ce2-96bb-117546cba275)


**THIS CONCLUDES THE FIRMWARE UPLOAD INSTRUCTIONS FOR THE ESP32 MARAUDER MINI**
**PLEASE PROCEED TO [TESTING](#testing)**

## Testing
The testing process is the same between the two referenced devices, ESP32 Marauder v6.1 and ESP32 Marauder Mini.
1. Download, install, and open [PuTTY](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)
2. Connect the flashed ESP32 Marauder PCB to your workstation using a USB-C cable  
![3FD2E498-E6A2-4ABF-AFFB-9FD5BE04A1DF - Copy](https://github.com/justcallmekoko/ESP32Marauder/assets/25190487/0506f24a-bb4e-42a1-b0c6-113dad670e4d)

3. Configure PuTTY to connect to the ESP32 Marauder PCB
    - Connection Type: `Serial`
    - Speed: `115200`
    - Serial Line:
        - Select the COM associated with the PCB's CP2102 chip. This can be done by locating the device in Device Manager
![image](https://github.com/justcallmekoko/ESP32Marauder/assets/25190487/6a555947-ec88-4827-b277-53119fd8be64)  
    - Your PuTTY window should now appear like the image below  
![image](https://github.com/justcallmekoko/ESP32Marauder/assets/25190487/d15c36f3-8d45-420a-bcc9-514870df3378)
4. Click `Open` and a new black window will appear
    - Once the new window opens, it may cause the firmware on the ESP32 to reset in which case you can skip step 5
5. Press the `RESET` button on the PCB  
![F18707AD-3E24-47BB-B2C2-14CA9295C846 - Copy](https://github.com/justcallmekoko/ESP32Marauder/assets/25190487/2bc8edaa-9fe2-430f-ab1a-8324f498e34f)

6. Monitor the PuTTY window to look for the output shown in the image below. It may take up to 20 seconds but no longer than 30
    - If the firmware upload was successful, you should see the following output
![image](https://github.com/justcallmekoko/ESP32Marauder/assets/25190487/e64a53e1-69dd-46d5-ba3f-865a39638d87)

**THIS CONCLUDES THE TESTING DOCUMENTATION**