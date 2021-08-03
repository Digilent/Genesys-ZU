Genesys ZU-3EG Out of Box Demo
==========================

Description
-----------
This repository contains the Out-of-Box Demo for the Genesys ZU-3EG. It is the same demo that comes preprogrammed on the microSD card when shipped to customers. The demo uses several test scripts that are build into the OS in order to access a wide range of 
the board's peripherals, including the Display Port, Ethernet, Mini PCIe, USB Type C, User IOs (LEDs, RGB LEDs, buttons, switches etc.). Depending the case, each test has 
different hardware requirements. For receiving feedback mesasges and controlling each individual test an MicroUSB cable needs to be connected between the computer and the USB/PROG port.
To successfully run the Display Port test, an Display port capable monitor is required, as well as one Display Port cable. If desired, an SSH connection can be established with the board by connecting it
to a router via an ethernet cable. The IP address of the board can be determined by using the command 'ip a' in the serial terminal. 
All the test scripts can be found in the /usr/bin directory, and are listed bellow:

| Test Name                                 | Description                                                |
| ---------------------------------------   | --------------------------------                           |
| DP-bist                                   | Displays a test pattern over DisplayPort                   |
| DP-bist-wrapper                           | Wraps DP-bist to allow it to run in the background         |
| network-bist                              | Tests the network connections through eth0 and wlan0 by bringing the interface up, requesting an IP address through DHCP and pinging the default gateway DHCP gives us. The first argument is the interface to test, `eth0` or `wlan0`. For `wlan0` two more arguments need to be provided, the SSID and PSK of the access point to associate with.                        |
| pci-bist                                  | Checks whether a specific device (Qualcomm QCA6174) is installed in the Mini PCIe slot.                              |
| rtc-test                                  | Tests the Real Time Clock                                  |
| sim-bist                                  | Querries the gammu utility for the presence of a SIM card. Needs a cellular modem installed in the Mini PCIe slot.                                 |
| sysmon                                    | Checks the temperature of the FPGA PL or the voltage on the power rails   |
| type-c-dir                                | Displays the orientation of the attached USB Type C cable.   |
| uio-test                                  | Tests several AXI GPIO peripherals tied to PL User IOs (LEDs, RGB LEDs, buttons, switches)    |
| usb-bist                                  | Tests onboard USB devices to see if they are being enumerated and brought up correctly    |
| usb-reset                                 | Resets all connected USB devices by unbinding and binding their drivers. This should also provide a hardware reset to the devices.     |
| wifi-bist                                 | Used by the network-bist script.      |
| zuca-test-suite                           | Wraps the other test scripts for testing in manufacturing. Requires modification to be run by a user.       |
 


Each test script will return it's own status messages. See the Requirements section below for instructions on how to log into the board and use an application to view these messages.

Requirements
------------
* **Genesys ZU-3EG**: To purchase a Genesys ZU-3EG, see the [Digilent Store](https://store.digilentinc.com/genesys-zu-zynq-ultrascale-mpsoc-development-board/).
* **Vivado 2020.1 Installation with Xilinx Vitis**: To set up Vivado, see the [Installing Vivado and Digilent Board Files Tutorial](https://reference.digilentinc.com/vivado/installing-vivado/start).
* **Serial Terminal Emulator Application**: For more information see the [Installing and Using a Terminal Emulator Tutorial](https://reference.digilentinc.com/learn/programmable-logic/tutorials/tera-term).
* **MicroUSB Cable**
* **Display Port cable (for the `DP-bist` script)**
* **Display Port capable Monitor/TV (for the `DP-bist` script)**
* **ETHERNET cable (for the `network-bist` script)**
* **Router (for the `network-bist` script)**
* **Qualcomm QCA6174 (for the `pci-bist` script)**
* **SIM card (for the `sim-bist` script)**
* **USB Type C cable (for the `type-c-dir` script)**


Demo Setup
----------
Note: At time of manufacturing, the programming mode select jumper is set to “SD”, and the microSD card with the Out-of-Box Petalinux image is placed in the microSD card slot. In order to get access to bugfixes
or changes made to the Out-of-Box demo and test scripts, or to view or change the demo, the corresponding repositories must be cloned and rebuilt. 

1. Repositories for the Out of the Box Demo can be found on Github, see the [Vivado project](https://github.com/Digilent/Genesys-ZU-HW/tree/3eg/master) and the [Petalinux Project](https://github.com/Digilent/genesys-zu-os/tree/3eg/master).
2. Connect the power supply.
3. Connect a computer to the USB/PROG port via the provided MicroUSB cable.
4. Flip the POWER switch to the ON position.
5. Connect a serial terminal to the serial port associated with the board with a baud rate of 115200.
6. Wait for the boot sequence to complete. If the serial terminal wasn't connected until after the board fully booted, the serial terminal will be blank. In this case, press enter to see the login prompt.
7. Log into the board with the username and password “root”. At this point, a command shell with root privileges has been opened into the Out-of-Box demo's PetaLinux OS. 
8. When finished using the Genesys ZU, make sure to safely shut down the OS through the shell.

Next Steps
----------
This demo can be used as a basis for other projects by modifying the hardware platform in the Vivado project's block design or by making changes to the test scripts.
Check out the Genesys ZU-3EG's [Resource Center](https://reference.digilentinc.com/programmable-logic/genesys-zu/start) to find more documentation, demos, and tutorials.
For technical support or questions, please post on the [Digilent Forum](forum.digilentinc.com).

Known Issues
------------
* None.

Additional Notes
----------------
For more information on how this project is version controlled, refer to the digilent-vivado-scripts submodule's [readme](https://github.com/digilent/digilent-vivado-scripts).