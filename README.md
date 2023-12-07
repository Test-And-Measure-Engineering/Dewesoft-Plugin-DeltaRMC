# Dewesoft-Plugin-DeltaRMC
A custom Dewesoft Plugin for Delta Motion RMC Controllers

# Installation Instructions
## Pre-Requisites
* Delta RMC Motion Controller
  * Delta Motion provides Online RMCs for testing and demonstration purposes. See their website for more information: *https://deltamotion.com/support/online-rmcs*
  * License keys for the Online RMCs are included. In the plugin setup, connect to the Online RMC by entering the hostname into the connection string e.g. *rmc150.deltamotion.com*
* RMCTools 64-bit
  * Download and install at *https://deltamotion.com/support/downloads*
* RMCLink 64-bit
  * Download and install at *https://deltamotion.com/support/downloads*
* DewesoftX 64-bit
  * Download and install at *https://dewesoft.com/download*
* DewesoftX License
  * All Dewesoft DAQ hardware includes a pro license. The hardware must be connected for the license to be active
  * An evaluation license may be obtained at *https://dewesoft.com/dewesoftx-licensing*
  * Contact your Dewesoft sales rep for more information on licensing
* DeltaRMC Plugin
  * Download the latest release from github repository *Test-And-Measure-Engineering / Dewesoft-Plugin-DeltaRMC*
* DeltaRMC Plugin License
  * A license is required for each Delta RMC Controller
  * Licenses are stored in the plugin directory as plaintext in the file *DeltaRMC.lic*
  * To obtain a plugin license, email *support@testandmeasure.engineering*

## Install Software
This section describes the steps needed to use this plugin. Here are the high-level steps:
1) Install RMCTools
2) Install RMCLink
3) Install DewesoftX
4) Install Plugin
5) Install Licenses
6) Configure RMC Controller
7) Configure Plugin
### RMCTools
* Download the 64-bit version of RMCTools from deltamotion.com
* Direct Link: https://deltamotion.com/files/rmctoolsinstall64.exe
### RMCLink
* Download the 64-bit version of RMCLink from deltamotion.com
* Direct Link: https://deltamotion.com/files/rmclinkinstall64.exe
### DewesoftX
* Download the 64-bit versino of DewesoftX from dewesoft.com
* Downloads Page Link: https://dewesoft.com/download
## Install Plugin
* Navigate to the plugin's github repository: https://github.com/Test-And-Measure-Engineering/Dewesoft-Plugin-DeltaRMC/
* From the repository, navigate to the Releases page:
![download_plugin_github_repo_page](https://github.com/Test-And-Measure-Engineering/Dewesoft-Plugin-DeltaRMC/assets/150857697/6a1d37f9-db02-4e91-8590-d031c34ba0d5)
* On the releases page, under the latest release's Assets, download the plugin by selecting *DeltaRMC.zip*:
![download_plugin_github_releases_page](https://github.com/Test-And-Measure-Engineering/Dewesoft-Plugin-DeltaRMC/assets/150857697/0c4c5e71-d28a-49bb-9869-95e6e6493c1f)
* Extract DeltaRMC.zip and copy the unzipped folder to the DewesoftX Bin64\Addons64 folder
* The resulting path should look like this: *C:\Program Files\DewesoftX\App\Bin64\Addons64\DeltaRMC*
* The DeltaRMC plugin folder should contain two files: DeltaRMC64.dll and DeltaRMC.lic
## Install Licenses
### DewesoftX
* A DewesoftX Pro license must be installed to use 3rd party plugins. 
 * All Dewesoft DAQ hardware includes a pro license. The hardware must be connected for the license to be active
 * An evaluation license may be obtained at *https://dewesoft.com/dewesoftx-licensing*
 * Contact your Dewesoft sales rep for more information on licensing
### Plugin
* A license must be purchased for each RMC controller
* Each license is registered with the MAC Address of the controller
* To get the MAC Address, follow these instructions from the RMCTools manual:
![controller_mac_address_instructions](https://github.com/Test-And-Measure-Engineering/Dewesoft-Plugin-DeltaRMC/assets/150857697/4571d27e-aad3-4be4-bd91-bda1c64af75c)
* In this example, the MAC Address is 00-50-A0-B1-1D-5A:
* ![controller_mac_address_example](https://github.com/Test-And-Measure-Engineering/Dewesoft-Plugin-DeltaRMC/assets/150857697/be028e3e-96ea-4241-ab11-ff75d2e2425e)
* After obtaining the MAC address
## Configure Controller
## Configure Plugin in Dewesoft

# Troubleshooting
## Invalid Dewesoft License
## Invalid Plugin License
## RMCLink COM Object - The RMCLink.dll COM server has not been registered
* This error means that RMCLink is not installed
* To fix this problem, install RMCLink
* See Install Software -> RMCLink for instructions
![RMCLink_COM_Not_Registered](https://github.com/Test-And-Measure-Engineering/Dewesoft-Plugin-DeltaRMC/assets/150857697/b1f60e64-70a5-48af-98f8-8c550bc7d68b)



