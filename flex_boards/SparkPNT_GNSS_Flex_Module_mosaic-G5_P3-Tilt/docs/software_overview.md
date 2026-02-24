## RxTools Software Suite
Users should install the [RXTools software suite](https://www.septentrio.com/en/products/gps-gnss-receiver-software/rxtools) on their computer to interface with the mosaic-G5 P3 GNSS receiver.


<article style="text-align: center;" markdown>
[:octicons-download-16:{ .heart } Download the RxTools Software from Septentrio](https://www.septentrio.com/en/products/gps-gnss-receiver-software/rxtools){ .md-button .md-button--primary target="blank" }
</article>


!!! info "System Requirements[^1]"

	<div class="grid cards" markdown>

	<div markdown>

	**Operating Systems**

	---

	- Windows 7
	- Windows 8
	- Windows 10
	- Fedora 23 *(or later)* using Qt technology.
		- The standalone tools (except `bin2asc`) will run on older distributions.

	</div>


	<div markdown>

	**Hardware Requirements**

	---

	The minimal hardware requirements *(1Hz update[^2])*:

	- CPU: 1 GHz processor
	- RAM: 1 GB RAM
	- Screen Resolution: 1024×768 or higher resolution

	</div>

	</div>


[^1]: The system requirements and installation instructions are from the RxTools *v22.1.0* user manual. This information may change in later iterations of the software suite. Please refer to the user manual *(of the version you are utilizing)* for the most accurate information.
[^2]: Higher data rates will require increased processing speed and memory capacity.



### Installation

=== "Windows"
	Users can install RxTools software suite by running the installation executable[^3] (`*.exe`), located in the `RxTools\windows` directory of the downloaded `*.zip` file[^4]. During the installation process, users will be notified if a previous version of RxTools is already installed then that the previous version will be uninstalled. Next, users will need to provide an installation directory for the RxTools software suite. Users will then select which of the following applications[^5] are installed:

	<!-- Create Break from Annotation (list won't render without comment)-->

	<div class="grid" markdown>

	<div markdown>

	- RxControl
	- SBF Converter
	- SBF Analyzer
	- RxLogger

	</div>

	<div markdown>

	- RxUpgrade
	- RxDownload
	- RxPlanner

	</div>

	<div markdown>

	- Data Link
	- RxAssistant
	- RxLauncher

	</div>

	</div>


=== "Linux"
	Users can install RxTools software suite by running the installation binary[^4] (`*.bin`), located in the `RxTools/linux-i386/` directory of the downloaded `*.zip` file[^4]. During the installation, users will be prompted for an installation directory. If there are any previous installations of RxControl, please use a different directory to avoid conflicts.


	!!! warning
		It is recommended that users **<span style="color:red">NOT</span>** install RxControl as `root`, for security reasons and to avoid installation overwrites of other system settings. To make RxTools available to more than one user, provide a shared installation directory.


	??? info "Permission Settings"
		Once installed, users may need to reconfigure their permission settings:

		<div class="annotate" markdown>

		- RxTools will need rights to access the `/dev/ttyS*` serial ports.

			- To access the serial ports, users must be part of the `uucp` and `lock` groups (1). This can be configured by editing the `/etc/group`[^6] file and adding the username to the lines defining the `uucp` group and the `lock` group.

				For example, when adding the user `jsmith` to the `uucp` group, users would modify the `/etc/group` file as shown below:

				```bash
				{--uucp:x:14:uucp--} # (2)!
				{++uucp:x:14:uucp,jsmith++} # (3)!
				```

			- On Linux machine administered centrally on a local network, ask your system administrator to be included in the `uucp` and `lock` groups.
		- RxTools also needs read/write (`rw`) access(4) to the `/dev/ttyS*` serial ports.

			- Users can change the permissions with the `chmod`[^7] command:

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


	??? tip "64-bit OS"
		In order to run the RxTools on a 64-bit Linux operating system, users might to install the 32-bit version of the `C` standard library.

		- For Fedora installations, this is the `glibc.i686` package.
		- The equivalent for Debian(/Ubuntu) installations is the `ia32-libs` package.


[^3]: Users will need administrative privileges to install the RxTools software.
[^4]: Users may need to extract the RxTools installation files from the downloaded, compressed file.
[^5]: Please see the release notes for the issues and limitations of the RxTools applications.
[^6]: Requires c privileges.
[^7]: Changing these permissions also requires `root` privileges.



## Serial Interface
Once connected through the USB interface, the mosaic-G5 P3 module emulates two virtual serial ports, which can be accessed as standard `COM` ports to the receiver.

!!! tip "Terminal Emulators"
	Most [terminal emulation programs](https://learn.sparkfun.com/tutorials/112) will not make a distinction between virtual or native COM ports. However, for virtual serial ports, the port settings *(i.e. baudrate, etc.)* are not relevant and the default configuration be used in the terminal emulation program. However, for the physical/native `COM` ports will have the following default setting:

	- Baudrate: 115200bps
	- Data Bits: 8
	- Parity: No
	- Stop Bits: 1
	- Flow Control: None
