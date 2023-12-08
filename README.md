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

## Overview
These are the high-level steps required to install and configure the plugin:
1) Install RMCTools
2) Install RMCLink
3) Install DewesoftX
4) Install Plugin
5) Add DewesoftX Pro License
6) Add Plugin Licenses
7) Configure RMC Controller
8) Configure Plugin

## Install RMCTools
* Download the 64-bit version of RMCTools from deltamotion.com
* Direct Link: https://deltamotion.com/files/rmctoolsinstall64.exe
* RMCTools is not required to use the plugin, but it is required to configure the data channels exposed by the controller

## Install RMCLink
* Download the 64-bit version of RMCLink from deltamotion.com
* Direct Link: https://deltamotion.com/files/rmclinkinstall64.exe

## Install DewesoftX
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

## Add DewesoftX Pro License
* A DewesoftX Pro license is required to use 3rd party plugins
* All Dewesoft DAQ hardware includes a pro license. Connect the hardware to the computer for the license to be active
* Alternatively, an evaluation license may be obtained at *https://dewesoft.com/dewesoftx-licensing*
* Contact your Dewesoft sales rep for more information on licensing

## Add Plugin Licenses
* A license is required for each RMC controller where each license is registered with the MAC Address of the controller
* To get a license, email *support@testandmeasure.engineering* for instructions
* When asked for the MAC address of the controller, follow these instructions from the RMCTools manual:
![controller_mac_address_instructions](https://github.com/Test-And-Measure-Engineering/Dewesoft-Plugin-DeltaRMC/assets/150857697/4571d27e-aad3-4be4-bd91-bda1c64af75c)
* For example, in the screenshot below, the MAC Address is 00-50-A0-B1-1D-5A:
![controller_mac_address_example](https://github.com/Test-And-Measure-Engineering/Dewesoft-Plugin-DeltaRMC/assets/150857697/be028e3e-96ea-4241-ab11-ff75d2e2425e)
* After obtaining the license, open DeltaRMC.lic with a text editor. DeltaRMC.lic is located in *DewesoftX\App\Bin64\Addons64\DeltaRMC*
* Paste the license key into DeltaRMC.lic. The resulting file should look like this, where each line is a licence key for a controller. Note that multiple licenses can be present:
![license_file](https://github.com/Test-And-Measure-Engineering/Dewesoft-Plugin-DeltaRMC/assets/150857697/23a9bfea-34e8-4c57-9dbe-7c33a2c61f7b)

## Configure Controller
* The plugin only records data that is configured through RMCTools Plots
* RMCTools is not required to use the plugin, but it is required to configure the data channels exposed by the controller
* To configure the data channels, open RMCTools, connect to the controller, and open *Plots Manager*
![rmc_tools_connect](https://github.com/Test-And-Measure-Engineering/Dewesoft-Plugin-DeltaRMC/assets/150857697/7e58a739-fc78-4770-a8bc-29e0253845a4)
* In the *Plots Manager*, click on *Edit Plot Templates*, to open the *Plot Template Editor*
![rmc_tools_plots_manager](https://github.com/Test-And-Measure-Engineering/Dewesoft-Plugin-DeltaRMC/assets/150857697/75db50c3-1074-4e27-9137-4453a90ffe45)
* In the *Plot Template Editor*, click the *+ Add* button to add a new plot
![rmc_tools_plot_template_editor_add_plot](https://github.com/Test-And-Measure-Engineering/Dewesoft-Plugin-DeltaRMC/assets/150857697/39ce2cf1-8a73-471d-b25a-d15be9591f1d)
* The next steps are for configuring the new plot
* First, change the plot to a *Custom Plot*
![](https://github.com/Test-And-Measure-Engineering/Dewesoft-Plugin-DeltaRMC/assets/150857697/ce8a064f-df79-4793-b0bc-b13fbe412da5)
* Next, select *Edit Trigger Settings*. The *Plot Trigger Setup* window will appear
![](https://github.com/Test-And-Measure-Engineering/Dewesoft-Plugin-DeltaRMC/assets/150857697/a7189db8-1829-4cf3-b4ea-67a65163cbcf)
* In the *Plot Trigger Setup* window, disable automatic trigger, select manual rearm, and confirm the pre-trigger percentage equals 0%
* Select *OK* on the *Plot Trigger Setup* window to confirm the trigger settings
![](https://github.com/Test-And-Measure-Engineering/Dewesoft-Plugin-DeltaRMC/assets/150857697/5af6124f-a160-476e-babe-24175b2e7c8e)
* Back on the *Plot Template Editor*, edit the timing settings
* *Sample Interval* is the rate at which the controller provides data to the plugin. Select the largest possible sample interval that meets your data rate requirements. Smaller values provide more data points, but may cause gaps in the data or delays in the UI update rate if the total data rate is too high relative to the network connection's latency between the controller and Dewesoft. The data rate is a function of sample interval and the number of plot templates
* *Capture Duration* is the size of the controller's internal buffer. This parameter has no effect on the plugin, unless very small values are used. It is usually best to make this number as large as possible
* *Trend Duration* is related only to RMCTools and not the controller or plugin. The value does not matter unless viewing trend plots in RMCTools
![](https://github.com/Test-And-Measure-Engineering/Dewesoft-Plugin-DeltaRMC/assets/150857697/b645ece6-9ead-4304-ad41-4ecf4fb671e2)
* Finally, edit the *Plotted Data Items*. The data items in this section will be automatically detected and recorded in the plugin
![](https://github.com/Test-And-Measure-Engineering/Dewesoft-Plugin-DeltaRMC/assets/150857697/56361c7e-73dd-40b3-9dc5-06858fb35c33)
* After configuring the plot, select *OK* in the *Plot Template Editor* to upload the plot settings to the controller. Note: you must be connected to the controller for the settings to take place


## Configure Plugin in Dewesoft

# Troubleshooting
## Invalid Dewesoft License
## Invalid Plugin License
## RMCLink COM Object - The RMCLink.dll COM server has not been registered
* This error means that RMCLink is not installed
* To fix this problem, install RMCLink
* See Install Software -> RMCLink for instructions
![RMCLink_COM_Not_Registered](https://github.com/Test-And-Measure-Engineering/Dewesoft-Plugin-DeltaRMC/assets/150857697/b1f60e64-70a5-48af-98f8-8c550bc7d68b)



