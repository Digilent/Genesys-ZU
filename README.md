# Genesys ZU Root Repository

## Genesys ZU-5EV HDMI Demo

### Description

This branch contains sources for the Genesys ZU-5EV HDMI Demo.

This project demonstrates usage of the Genesys ZU-5EV's HDMI in and HDMI out ports. Vivado is used to build the demo's hardware platform, and Vitis is used to program the bitstream onto the board and to build and deploy a C application.

To use this demo, the Genesys ZU-5EV must be connected to a computer over MicroUSB, which must be running a serial terminal.

A menu is displayed over UART at 115200 baud rate. When only the HDMI TX port is connected, the project enters in standalone mode, generating a color bar on the display. 
When both HDMI ports are connected, and there is a valid HDMI source, the project will automatically enter in pass-through mode and the Si5342A-D-GM will generate a jitter-attenuated reference clock to drive the HDMI Transmitter Subsystem with a phase-aligned version of the HDMI RX Subsystem HDMI RX TMDS Clock. Thus, the image from the HDMI source will be outputted on the display.

For more information on the Genesys ZU-5EV HDMI Demo, including setup instructions, visit its [Demo Page](https://reference.digilentinc.com/learn/programmable-logic/tutorials/genesys-zu-5ev-demo-hdmi/start) on the Digilent Wiki.

For more information on the Genesys ZU, including other demos that may be available, see its [Resource Center](https://reference.digilentinc.com/reference/programmable-logic/genesys-zu/start) on the Digilent Wiki.

### Git Navigation Information

For instructions on how to use this repository with git, and for additional documentation on the submodule and branch structures used, please visit [Digilent FPGA Demo Git Repositories](https://reference.digilentinc.com/reference/programmable-logic/documents/git) on the Digilent Wiki. Note that use of git is not required to use this demo. Digilent recommends the use of project releases, for which instructions can be found in each demo wiki page, linked above.

To see other demos in this repository, see the master branch's [README](https://github.com/Digilent/Genesys-ZU).

Some demos do not require some submodules, in these cases, they are still provided to ease switching between demos in git. When unused, the submodule folder is largely empty, except for a readme containing only the heading "Root commit". This demo contains the following submodules:

| Submodule | Used by this demo |
|-----------|-------------------|
| HW        | Yes      |
| OS        | No       |
| SW        | Yes      |

### Requirements

The following are required for use of this demo. For more information on how to get any hardware or software you may be missing, see the Demo Page, linked above.


* Genesys ZU-5EV FPGA board
* 1 Micro-USB cables
* Genesys ZU-5EV Power Supply
* 1 or 2 HDMI-HDMI or HDMI-DVI Cables
* 1 HDMI Display
* 1 HDMI Source (Used only in pass-through mode)
