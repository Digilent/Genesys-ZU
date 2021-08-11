Genesys ZU-5EV Base Demo
==========================

Description
-----------
This repository contains the Base Demo for the Genesys ZU-3EG. It is a simple demo that configures the Zynq Ultrascale+ MPSoc with the given board file, and outputs "Hello World" on the serial terminal. For receiving the message, an MicroUSB cable needs to be connected between the computer and the USB/PROG port.

Requirements
------------
* **Genesys ZU-3EG**: To purchase a Genesys ZU-3EG, see the [Digilent Store](https://store.digilentinc.com/genesys-zu-zynq-ultrascale-mpsoc-development-board/).
* **Vivado 2020.1 Installation with Xilinx Vitis**: To set up Vivado, see the [Installing Vivado and Digilent Board Files Tutorial](https://reference.digilentinc.com/vivado/installing-vivado/start).
* **Serial Terminal Emulator Application**: For more information see the [Installing and Using a Terminal Emulator Tutorial](https://reference.digilentinc.com/learn/programmable-logic/tutorials/tera-term).
* **MicroUSB Cable**

Demo Setup
----------
In order to view or change the demo, the corresponding repositories must be cloned and rebuilt. 

1. Repositories for the Base Demo can be found on Github, see the [Vivado project](https://github.com/Digilent/Genesys-ZU-HW/tree/3eg/master)
2. Connect the power supply.
3. Connect a computer to the USB/PROG port via the provided MicroUSB cable.
4. Flip the POWER switch to the ON position.
5. Connect a serial terminal to the serial port associated with the board with a baud rate of 115200.
6. Launch Hardware from Xilinx SDK. This will load the program into the arm processor and will run the "Hello World!" program.


Next Steps
----------
This demo can be used as a basis for other projects by modifying the hardware platform in the Vivado project's block design.
Check out the Genesys ZU-3EG's [Resource Center](https://reference.digilentinc.com/programmable-logic/genesys-zu/start) to find more documentation, demos, and tutorials.
For technical support or questions, please post on the [Digilent Forum](forum.digilentinc.com).

Known Issues
------------
* None.

Additional Notes
----------------
For more information on how this project is version controlled, refer to the digilent-vivado-scripts submodule's [readme](https://github.com/digilent/digilent-vivado-scripts).
