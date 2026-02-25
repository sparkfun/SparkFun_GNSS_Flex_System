!!! note
	The system requirements and installation instructions are from the RxTools *v22.1.0* user manual. This information may change in later iterations of the software suite. Please refer to the user manual *(of the version you are utilizing)* for the most accurate information.


# RxTools Software Suite

Users should install the [RXTools software suite](https://www.septentrio.com/en/products/gps-gnss-receiver-software/rxtools)[^1] on their computer to interact with the mosaic-G5 P3 GNSS receiver through the USB interface. For Windows PCs, it also includes the USB driver for the GNSS receiver that enables the virtual `COM` ports[^2].


[^1]: The system requirements and installation instructions are from the RxTools *v22.1.0* user manual. This information may change in later iterations of the software suite. Please refer to the user manual *(of the version you are utilizing)* for the most accurate information.
[^2]: On Linux, the standard Linux CDC-ACM driver is suitable.


<article style="text-align: center;" markdown>
[:octicons-download-16:{ .heart } Download the RxTools Software from Septentrio](https://www.septentrio.com/en/products/gps-gnss-receiver-software/rxtools){ .md-button .md-button--primary target="blank" }
</article>



## System Requirements

<div class="grid" markdown>

<div markdown>

### Operating System

---

* Windows 7
* Windows 8
* Windows 10
* Fedora 23 *(or later)* using Qt technology.
	* The standalone tools (except `bin2asc`) will run on older distributions.

</div>

<div markdown>

### Hardware Requirements

---

The minimal hardware requirements *(1Hz update[^3])*:

* CPU: 1 GHz processor
* RAM: 1 GB RAM
* Screen Resolution: 1024×768 or higher resolution

</div>

</div>


[^3]: Higher data rates will require higher CPU speed and more memory capacity.



## Installation Instructions

=== "Windows"
	Users can install RxTools software suite by running the installation executable[^4](1), located in the `RxTools\windows` directory of the downloaded `*.zip` file[^5]. During the installation process, users will be notified if a previous version of RxTools is already installed then that the previous version will be uninstalled. Next, users will need to provide an installation directory for the RxTools software suite. Users will then select which of the following applications[^6] are installed:
	{ .annotate }

	1. For RxTools v22.1.0, the installation filename is `RxTools_22_1_0_Installer.exe` for Windows PCs.

	<!-- Create Break from Annotation (list won't render without comment)-->

	<div class="grid" markdown>

	<div markdown>

	* RxControl
	* SBF Converter
	* SBF Analyzer
	* RxLogger

	</div>

	<div markdown>

	* RxUpgrade
	* RxDownload
	* RxPlanner

	</div>

	<div markdown>

	* Data Link
	* RxAssistant
	* RxLauncher

	</div>

	</div>


=== "Linux[^2]"
	!!! warning
		It is recommended that users **<span style="color:red">NOT</span>** install RxControl as `root`, for security reasons and to avoid installation overwrites of other system settings. To make RxTools available to more than one user, provide a shared installation directory.

	Users can install RxTools software suite by running the installation binary[^4](1), located in the `RxTools/linux-i386/` directory of the downloaded `*.zip` file[^5]. During the installation, users will be prompted for an installation directory. If there are any previous installations of RxControl,  please use a different directory to avoid conflicts.
	{ .annotate }

	1. For RxTools v22.1.0, the installation filename is `RxTools_22_1_0_Installer.bin` for Linux.

	??? info "Permission Settings"
		Once installed, users may need to reconfigure their permission settings:

		<div class="annotate" markdown>

		* RxTools will need rights to access the `/dev/ttyS*` serial ports.

			* To access the serial ports, users must be part of the `uucp` and `lock` groups (1). This can be configured by editing the `/etc/group`[^7] file and adding the username to the lines defining the `uucp` group and the `lock` group.

				For example, when adding the user `jsmith` to the `uucp` group, users would modify the `/etc/group` file as shown below:

				```bash
				{--uucp:x:14:uucp--} # (2)!
				{++uucp:x:14:uucp,jsmith++} # (3)!
				```

			* On Linux machine administered centrally on a local network, ask your system administrator to be included in the `uucp` and `lock` groups.
		* RxTools also needs read/write (`rw`) access(4) to the `/dev/ttyS*` serial ports.

			* Users can change the permissions with the `chmod`[^8] command:

				```bash
				chmod 660 /dev/ttyS<add port> # (5)!>
				```

		</div>

		1. On most Linux operating systems, the `/dev/ttyS*` devices are owned by `root` and belong to the `uucp` group with read/write (`rw`) access. Additionally, the devices are normally locked by writing a file in the `/var/lock/` directory, with the same permissions.
		2. Remove
		3. Replace with this line
		4. By default, users will normally have read/write (`rw`) access to the `/dev/ttyS*` serial ports.
		5. where users must specify the port number<br>*e.g. `/dev/ttyS0` might be port `COM1`*

		!!! note
			In order for these changes to take effect, users must update their environment by logging out and back in.

			Be aware that the X-session has to be restarted as well. On most systems, this can be done by pressing the key combination ++ctrl++ + ++alt++ + ++backspace++

	??? info "64-bit OS"
		In order to run the RxTools on a 64-bit Linux operating system, users might to install the 32-bit version of the `C` standard library.

		* For Fedora installations, this is the `glibc.i686` package.
		* The equivalent for Debian(/Ubuntu) installations is the `ia32-libs` package.


[^4]: Users will need administrative privileges to install the RxTools software.
[^5]: Users may need to extract the RxTools installation files from the downloaded, compressed file.
[^6]: Please see the release notes for the issues and limitations of the RxTools applications.
[^7]: Requires c privileges.
[^8]: Changing these permissions also requires `root` privileges.

## Getting Started

=== "Windows"
	Once **RxTools** have been installed, any of the individual GUI tools can be launched using the **RxLauncher** application.

	When connecting to a receiver using USB, two virtual serial ports will be created on your machine which can be used to communicate to the receiver.

	* Check the Device Manager to see the exact names of these virtual serial ports.
		* They ports will appear with the name `Septentrio` written beside them.
	* These virtual serial ports will be labeled as such when **RxControl** shows the Connection Dialog.

	!!! tip
		The virtual serial port names correspond to a given USB port. When plugging the device into a different USB port, the serial port will change.

=== "Linux"
	Once **RxControl** is installed, it can be launched by executing the link created by the installation program or by executing `./runRxControl` in the directory where the program is installed.

	* The **Data Link** and **SBF Converter** applications should be executed from the `/bin` directory of the installation folder, to ensure that the proper libraries are loaded. Users can also run these applications from the installation directory, in a manner similar to **RxControl** that is described above.
	* Other applications can also be executed by launching their appropriate script.
		* For example, users can execute `./runDataLink` from the `/bin` directory, located inside the installation folder.



## Update Firmware
!!! info "Latest Firmware"
	For the latest firmware released by Septentrio, please visit their [product page](https://www.septentrio.com/en/products/gnss-receivers/gnss-receiver-modules/mosaic-G5-P3#resources) for the mosaic-G5 P3 GNSS receiver.

<div class="grid cards" markdown>

-   To check for the latest firmware published by Septentrio, please visit their [product page](https://www.septentrio.com/en/products/gnss-receivers/gnss-receiver-modules/mosaic-G5-P3#resources) for the mosaic-G5 P3 GNSS receiver. Users can click on the button below, to be redirected to the latest firmware for the mosaic-G5 P3.

	<article style="text-align: center;" markdown>
	[:septentrio: Find the Latest Firmware](https://www.septentrio.com/en/products/gnss-receivers/gnss-receiver-modules/mosaic-G5-P3#resources){ .md-button .md-button--primary target="blank" }
	</article>

-   Currently, at the time that this board was released, the firmware for the mosaic-G5 P3 GNSS receiver was *v1.0.1*[^4]. Users can download [**version 1.0.0**](./assets/component_documentation/firmware/v1.0.1/mosaic-G5%20P3_fwp_1.0.1.zip) of the firmware, by clicking on the button below.

	[^4]:
		For the latest firmware published by Septentrio, please visit their [product page](https://www.septentrio.com/en/products/gnss-receivers/gnss-receiver-modules/mosaic-G5-P3#resources).<br>
		*This is firmware version, was archived at the time that this guide was written. Please do not request for the file to be updated; instead visit the product page to download the latest firmware.*

	<article style="text-align: center;" markdown>
	[:octicons-download-16:{ .heart } Download Firmware *(v1.0.1)*](./assets/component_documentation/firmware/v1.0.1/mosaic-G5%20P3_fwp_1.0.1.zip){ .md-button .md-button--primary target="blank" }
	</article>

</div>


Below are the methods for upgrading the receiver:

1. Double click on the Septentrio firmware file with the `*.suf` extension. This should launch the **RxUpgrade** program.
2. Using the graphical interface of the **RxControl** program. Navigate to the **File** drop-down menu.
3. Manually upload the firmware file to the GNSS receiver.


### Manual Uplaod
Below are the instructions for manually uploading firmware to the GNSS receiver:

1. Enter the following command to set the receiver into upgrade mode:

	```
	exeResetReceiver, Upgrade, none
	```

2. Wait till the receiver outputs the string:

	```
	Ready for SUF download...
	```

3. From that moment on, the receiver is waiting for an upgrade file to be downloaded. The file download must start with in 200 seconds, otherwise the receiver will restart in normal mode.
3. Download the upgrade file to the receiver. Any of the receiver connections can be used. Make sure to send the file in binary mode, i.e. without changing its contents. During the download, the receiver outputs a progress indicator at regular intervals.
4. At the end of the download, the receiver automatically executes the upgrade instructions and restarts with the new firmware version. You can check the firmware version by entering the following command:

	```
	lif,Identification
	```


!!! info
	Before executing the upgrade instructions, the receiver checks the integrity of the downloaded file. If the file is corrupted, or is not a valid upgrade file, the receiver discards it and restarts in normal mode.


!!! warning
	- In some cases, upgrading the GNSS firmware can clear the receiver configuration stored in non-volatile memory. It is therefore advised to recheck the configuration after the upgrade.
	- If the download is interrupted for any reason, the receiver will restart in normal mode after a timeout period of 200 seconds.
	- Do not switch power off during the upgrade procedure.
	- Upgrading the receiver over a serial port can be very slow and it is recommended to upgrade using a faster connection whenever possible (USB).
