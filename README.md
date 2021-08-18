# Genesys ZU Root Repository

This repository contains all demos for the Genesys ZU.

For more information about the Genesys ZU, visit its [Resource Center](https://reference.digilentinc.com/programmable-logic/genesys-zu/start) on the Digilent Wiki.

Each demo contained in this repository is documented on the Digilent Wiki, links in the table below.

| Wiki Link | Demo Master Branch | Submodules Used |
|-----------|--------------------|-----------------|
| [Genesys ZU-5EV HDMI Demo](https://reference.digilentinc.com/learn/programmable-logic/tutorials/genesys-zu-5ev-demo-hdmi/start) | 5ev/demo/hdmi/master  | HW, SW |
| [Getting Started with the Genesys ZU (Out-of-Box Demo)](https://reference.digilentinc.com/programmable-logic/genesys-zu/getting-started) | 5ev/oob/master  | HW, OS |
| [Getting Started with the Genesys ZU (Out-of-Box Demo)](https://reference.digilentinc.com/programmable-logic/genesys-zu/getting-started) | 3eg/oob/master  | HW, OS |
| [Genesys ZU-5EV Hello World Demo](https://reference.digilentinc.com/learn/programmable-logic/tutorials/genesys-zu-demo-hello-world/start) | 5ev/master  | HW, SW |
| [Genesys ZU-3EG Hello World Demo](https://reference.digilentinc.com/learn/programmable-logic/tutorials/genesys-zu-demo-hello-world/start) | 3eg/master  | HW, SW |


## Repository Description

This repository is designed to offer a unified and comprehensive approach to all of the aspects of the demos that we provide for the Genesys ZU, across multiple tools. By cloning this repo recursively you will receive the repositories for Vivado projects (HW), Vitis workspaces (SW), and Petalinux projects (OS). Each submodule may have its own submodule dependencies which will also be pulled when cloning. An important aspect of this structure is the fact that the SW and OS heavily depend on hardware hand-off files from the HW repository.

This repository also provides releases containing project and image files used by the various tools involved. Releases provide files that are directly usable, without requiring the use git or any scripting systems. Documentation of each demo, as well as instructions for using their releases, can be found by visiting the corresponding pages on the Digilent Wiki, links below. All releases in this repository can be found in this repository's [releases page](https://github.com/Digilent/Genesys-ZU/releases), however, use of the wiki pages to find specific well-tested releases is advised.

For instructions on how to use this repository with git, and for additional documentation on the submodule and branch structures used, please visit [Digilent FPGA Demo Git Repositories](https://reference.digilentinc.com/reference/programmable-logic/documents/git) on the Digilent Wiki. Note that use of git is not required to use this demo.
