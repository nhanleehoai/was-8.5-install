# webspere-liberty-install
Guide on how to install Wesphere Liberty on Centos server


### Prerequsites

1. A remote server installed with Centos 7.x, VNC server
2. A Windows box with VNC viewer to connect to the server


### Get stated

- 1. Connect to the remote Centos server by VNC viewer
- 2. Download the IBM Installation Manger package

Click on the [link](https://download4.boulder.ibm.com/sdfdl/v2/sar/CM/RA/07hnt/0/Xa.2/Xb.jusyLTSp44S0MSxfbSR0jFZljMoCmsArctlgm3mZ38PsEPzElM8pGIWbvuk/Xc.CM/RA/07hnt/0/agent.installer.linux.gtk.x86_64_1.8.9000.20180313_1417.zip/Xd./Xf.LPR.D1VC/Xg.9721396/Xi.habanero/XY.habanero/XZ.wIAV7ge4CRRXyydTiF07Ro1fQw4/agent.installer.linux.gtk.x86_64_1.8.9000.20180313_1417.zip)
 
Install IBM Installation Manager. This is a tool which can be used to install many differrent IBM Websphere products

Check the folder 

<img src="docs/1-installation-manager-foler.png" />

- 3. Install the "IBM Installation Manager"

```
	./install
```
<img src="docs/2-installation-manager.png" />

Accept the License Agreement and next

<img src="docs/2-installation-manager-step2.png" />

- 4. Install Websphere Server 8.5

+ Launch the IBM Installation Manager

<img src="docs/3-installation-manager-launched.png" />
+ Click on the "Install" icon
+ Click on "Repositories" link

<img src="docs/4-select-repos.png" />

Wait for while so that the installer manager fetch all meta form the repositories

<img src="docs/5-select-was-8.5-toinstall.png" />

Select “IBM WebSphere Application Server for Developers (ILAN)” from the list
In the next screen, all recommended are selected/checked
Click “Next” and wait

<img src="docs/6-install-location.png" />

Select additional languages if needed

<img src="docs/7-install-features.png" />

Click “Next” on the next screen

<img src="docs/8-install-summary.png" />

Wait for the installation manager to download the selected products package
<img src="docs/9-installing.png" />

Take a cup of coffee and wait for the installer to download the files to install.

<img src="docs/10-install-done.png"/>

- 5. Create a new profile
<img src="docs/11-profile-step1.png"/>
<img src="docs/12-profile-step2.png"/>
<img src="docs/13-profile-step3.png"/>
<img src="docs/14-profile-step4.png"/>

Wait for the profile to be created

<img src="docs/15-profile-step5.png"/>


<img src="docs/16-first-step.png"/>

The profile has been created. Now check it: Click on “Start the server”

<img src="docs/17-first-step-1.png"/>
<img src="docs/18-first-step-2.png"/>


- 6. Verify the installation
<img src="docs/19-administrative.png"/>
<img src="docs/20-administrative-2.png"/>

<img src="docs/21-hello.png"/>

After the server restarted, use this command to start WebSphere again
```
/opt/IBM/WebSphere/AppServer/profiles/AppSrv01/bin/startServer.sh server1
```








