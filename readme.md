# MindSphere Remote Service - Quick Start Help
To allow you a quick start on the device-side of your remote service application using MindSphere, this repository contains some helpful information in order to setup your clients. 
<!-- Insert an example image -->
<!-- ![image](./doc/example.png) -->

- [MindSphere Remote Service - Quick Start Help](#mindsphere-remote-service---quick-start-help)
  - [Prerequisites](#prerequisites)
  - [Setup & Configuration](#setup--configuration)
    - [Debian](#debian)
    - [Windows](#windows)
  - [Result](#result)
  - [See also](#see-also)

## Prerequisites
- Access to MindSphere Remote Service App
- Debian based device which should be connected via MindSphere Remote Service

## Setup & Configuration

### Debian
To use the MRS client on a Debian based system, download the respective client from your MRS app on MindSphere as shown in the documentation. Next, store the client on the device and then start the service. The following step-by-step guide will help you doing so.

1. On your device, browse to directory where the MRS-Client .tar.gz file is located
2. Expand the archive-file (=unpack)
3. Change access rights to the mrs-client using if needed
    ```sudo chmod +x mrs-client```
4. Start the client using ```sudo ./mrs-client```
5. After the client is running, you need to accept the terms using ```y```(es), then the following screen should occur.  
   ![MRS device client running](/doc/MRS_running.png) 

> **_NOTE:_**  By default, the device client does not have an autostart function enabled. Meaning everytime the device is e.g. restarted, the client needs to be started manually again. 
> To change this behaviou, follow herebelow described setup. 

Optional: **Enable autostart**
To make the client run automatically, e.g. after a power-out of the device, a service needs to be registered in Debian for this. 
Please note that this mechanism is not formally supported but a community contribution. For production usage, no liabiltiy is taken, neither support provided. Consulting of a skilled Debian developer is highly recommended and the guide below just serves as helper. 
1) copy the [MRS_autostart_installer](/resources/setup.sh) to the directoy of the unzipped MRS device client. 
2) change access rights with ```sudo chmod +x setup.sh``` and run the installer using ```./setup.sh```

You should then find the client in the list of services of you system. 
![MRS running as service](/doc/MRS_client_as-Service.png)

Do uninstall/disable autostart, simply run [MRS_autostart_uninstaller](/resources/uninstall.sh) from the directory where you previously executed the ```./setup.sh``` from. 

### Windows  
... to follow later

## Result
Successfull installation/or running of the client can also be checked easily right on MindSphere using the online-status indicator in the MRS application. 
![MRS running as service](/doc/MRS_device_view_ONLINE.png)


## See also
- [:books: MindSphere Remote Service Documentation](https://documentation.mindsphere.io/MindSphere/apps/mrs-overview/mrs-overview.html) 
- [:shopping_cart: MindSphere Store: Remote Service](https://www.dex.siemens.com/mindsphere/step-4-book-apps-and-extras/remote-services) 


