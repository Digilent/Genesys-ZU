Genesys ZU-5EV SATA Base Demo
==========================

Description
-----------
This repository contains the SATA Base Demo for the Genesys ZU-5EV. It is a simple demo that configures the Zynq Ultrascale+ MPSoc with the given board file, and enables SATA on GT lane 0 instead of PCIe. It is an example base project to be used with Petalinux.

For more information on the Genesys ZU-5EV, including other demos that may be available, see its [Resource Center](https://reference.digilentinc.com/programmable-logic/genesys-zu/start) on the Digilent Wiki.

Requirements
------------
* **Genesys ZU-5EV**: To purchase a Genesys ZU-5EV, see the [Digilent Store](https://store.digilentinc.com/genesys-zu-zynq-ultrascale-mpsoc-development-board/).
* **Vivado 2020.1 Installation with Petalinux 2020.1: To set up Vivado, see the [Installing Vivado and Digilent Board Files Tutorial](https://reference.digilentinc.com/vivado/installing-vivado/start).
* **Serial Terminal Emulator Application**: For more information see the [Installing and Using a Terminal Emulator Tutorial](https://reference.digilentinc.com/learn/programmable-logic/tutorials/tera-term).
* ** Win32 Disk Imager or Rufus or other similar tool
* **MicroUSB Cable**

Demo Setup
----------
In order to view or change the demo, the corresponding repositories must be cloned and rebuilt. 

1. Repositories for the Base Demo can be found on Github, see the [Vivado project](https://github.com/Digilent/genesys-zu-hw/tree/5ev/sata/master) and the [Petalinux project](https://github.com/Digilent/genesys-zu-os/tree/5ev/sata/master).
2. Write the image **genesys-zu-5ev-sata.img** found in **5ev/sata release** to an SD card (use Win32 Disk Imager)
3. Insert the microSD card containing the Petalinux image into the microSD card slot.
4. Select the programming mode jumper to “SD”
5. Connect the power supply.
6. Connect a computer to the USB/PROG port via the provided MicroUSB cable.
7. Flip the POWER switch to the ON position.
8. Connect a serial terminal to the serial port associated with the board with a baud rate of 115200.
9. Wait for the boot sequence to complete. If the serial terminal wasn't connected until after the board fully booted, the serial terminal will be blank. In this case, press enter to see the login prompt.
10. Log into the board with the username and password “root”. At this point, a command shell with root privileges has been opened into the SATA demo's PetaLinux OS.
11. When finished using the Genesys ZU, make sure to safely shut down the OS through the shell.


Next Steps
----------
This demo can be used as a basis for other projects by modifying the hardware platform in the Vivado project's block design.
Check out the Genesys ZU-5EV's [Resource Center](https://reference.digilentinc.com/programmable-logic/genesys-zu/start) to find more documentation, demos, and tutorials.
For technical support or questions, please post on the [Digilent Forum](forum.digilentinc.com).

Known Issues
------------
* None.
