## GNSS Software
!!! tip
	While it is not required, we highly recommend that users configure their LG290P GNSS module with the [QGNSS software provided by Quectel](#qgnss-software). This is due to the unique data structure of the UART command messages, utilized to configure the LG290P module.


	??? warning "Windows Only"
		Currently, the QGNSS software is only available for Windows operating systems.


	??? success "Windows, MacOS, or Linux"
		For users with computers that run on MacOS or Linux, we have found alternative software option for viewing the data from the NMEA messages. However, this GUI interface is currently limited to only receiving UART messages and cannot send messages to configure the LG290P module.

		- :material-github: [GitHub Repository](https://github.com/semuconsulting/PyGPSClient)
		- [Installation Instructions](https://github.com/semuconsulting/PyGPSClient?tab=readme-ov-file#installation)
		- [PyPI Project](https://pypi.org/project/pygpsclient/)



## QGNSS Software
!!! warning "Windows Only"
	Currently, the QGNSS software is only available for Windows operating systems.


QGNSS is highly intuitive GNSS evaluation software that is easy to use, personalized, and compatible with leading Quectel technologies. The software allows users to define or apply GNSS product configurations for specific use cases. Saving, restoring, or sharing configurations between different products and users is easy. The software supports product evaluation with a choice of views to observe static and dynamic behavior of the connected a Quectel GNSS receiver.


<center>
[:octicons-download-16:{ .heart } Download the QGNSS Software *(v2.0)* from Quectel](https://www.quectel.com/download/qgnss_v2-0_en/){ .md-button .md-button--primary target="blank" }
</center>


!!! info "System Requirements"
	**Operating System:** Windows



### Connecting to the LG290P
In order to connect to the LG290P properly, users will need USB-to-Serial converter to connect to one of the LG290P's UART ports.


<figure markdown>
[![Configure UART Settings](./assets/img/hookup_guide/qgnss-uart_settings-button.png){ width="400" }](./assets/img/hookup_guide/qgnss-uart_settings-button.png "Click to enlarge")
<figcaption markdown>
Click the <kbd>:material-cog:</kbd> button to configure the UART settings.
</figcaption>
</figure>


Before users can connect to the LG290P GNSS Flex module, they will need to specify the connection settings in QGNSS. Once configured, users can select the ++"OK"++ button and QGNSS will automatically attempt to connect to the GNSS module.


- Select the `LG290P(03)` from the drop-down menu to configure the `Model` of the GNSS module being connected.
- Below, is a list of the default settings for `UART` ports of the LG290P. These settings should be selected in the `Device Information` menu, unless configured differently.
- For the `Port`, select the port associated with the attached USB-to-Serial converter.


<div class="grid" markdown>

<div markdown>

<figure markdown>
[![UART Settings in QGNSS](./assets/img/hookup_guide/qgnss-uart_settings.png){ width="400" }](./assets/img/hookup_guide/qgnss-uart_settings.png "Click to enlarge")
<figcaption markdown>
Specify the settings for the UART port in QGNSS.
</figcaption>
</figure>

</div>


<div markdown>

!!! info "LG290P - Default Settings"
	The UART ports of the LG290P GNSS module will have the following default configuration:

	- Baudrate: 460800bps
	- Data Bits: 8
	- Parity: No
	- Stop Bits: 1
	- Flow Control: None

</div>

</div>



### Configure the LG290P
By default, the UART ports are configured to transmit and receive `NMEA 0183` and/or `RTCM 3.x` messages. These messages are generally used for transmitting PNT data; and providing or receiving RTK corrections, respectively. Quectel also implements a system of proprietary messages (`PQTM`) for users to configure the LG290P, following the data format of the `NMEA` protocol.

???+ terminal "Data Format - PQTM Messages"
	The expected structure of the data in the proprietary PQTM messages is shown below:

	<figure markdown>
	[![NMEA data structure](./assets/img/hookup_guide/nmea_protocol.png){ width="600" }](./assets/img/hookup_guide/nmea_protocol.png "Click to enlarge")
	<figcaption markdown>
	The data structure of Quectel messages for the `NMEA` protocol.
	</figcaption>
	</figure>


	`<Checksum>`:

	- Checksum field follows the checksum delimiter character `*`.
	- Checksum is the 8-bit exclusive OR of all characters in the sentence, including `,` the field delimiter, between but not including the `$` and the `*` delimiters.

	`<CR>` & `<LF>`: Carriage return; followed by a new line

	- Depending on the terminal emulator, these may be options configured in the program settings.
	- Otherwise, users may need to add the `\r` and `\n` characters at the end of the message.


In the QGNSS software, users can click on the ++"Advance"++ button, at the bottom of the `QConsole` window, to configure the settings for the messages sent to the LG290P. Selecting `NMEA` and `CRLF` from the drop-down menu of the **Checksum Type** and **Suffix** options, will automatically calculate and append the `<checksum>` value, carriage return, and line follow to the end of the message entered in the **Data Input** field.


<figure markdown>
[![NMEA message setting](./assets/img/hookup_guide/qgnss-message_settings.png){ width="600" }](./assets/img/hookup_guide/qgnss-message_settings.png "Click to enlarge")
<figcaption markdown>
The settings for the messages transmitted from the QConsole.
</figcaption>
</figure>


???+ tip "Display the QConsole Toolbar"
	There is a toolbar for the QConsole, which has a bunch of tools that users may find useful. This includes, a search function, scroll-lock button, pause/clear the message feed, etc. To open/close the toolbar inside the QConsole, ++"right-click"++ on the mouse and select the `Show Tool` option from the drop-down menu or utilize the keyboard shortcut: ++ctrl++ + ++q++.


	<figure markdown>
	[![QConsole Toolbar](./assets/img/hookup_guide/qgnss-toolbar.gif){ width="400" }](./assets/img/hookup_guide/qgnss-toolbar.gif "Click to enlarge")
	<figcaption markdown>
	++"Right-click"++ on the mouse and select the `Show Tool` option, inside the QConsole.
	</figcaption>
	</figure>


??? example "Example - `PQTMCFGUART` Message"
	As an example, try utilizing the `PQTMCFGUART` PQTM message. Enter `$PQTMCFGUART,R*` into the **Data Input*** field of the QConsole. DOn't forget to select the `NMEA` and `CRLF` options from ++"Advance"++ settings menu. If entered and configured properly, the value `36` should pop up in the **Checksum** field of the QConsole; then, click on the <kbd>:material-send:</kbd> button to send the message.


	``` bash
	$PQTMCFGUART,R*
	```


	Once the message has been sent, keep a close watch of the messages in the console. It may help to click on the <kbd>:octicons-unlock-16:</kbd> button to disable auto-scrolling, when trying to locate the message response. Additionally, the response may not appear right away, it could be appended to the end of the next data packet, as shown in the image below.


	<figure markdown>
	[![PQTM demo](./assets/img/hookup_guide/qgnss-pqtm_message.png){ width="400" }](./assets/img/hookup_guide/qgnss-pqtm_message.png "Click to enlarge")
	<figcaption markdown>
	Example of utilizing the Quectel PQTM messages in the QConsole.
	</figcaption>
	</figure>



## PyGPSClient
As an alternative to QGNSS, we recommend [PyGPSClient](https://github.com/semuconsulting/PyGPSClient) for users with computers that run on MacOS or Linux.


??? info "Resources"
	For additional information, users can refer to the following resources for the PyGPSClient software:

	- :material-github: [GitHub Repository](https://github.com/semuconsulting/PyGPSClient)
	- [Installation Instructions](https://github.com/semuconsulting/PyGPSClient?tab=readme-ov-file#installation)
	- [PyPI Project](https://pypi.org/project/pygpsclient/)



### Installation
There are a variety of [installation methods](https://github.com/semuconsulting/PyGPSClient?tab=readme-ov-file#installation) detailed in the GitHub repository's `README.md` file. However, we recommend utilizing the `pip` installation method.


!!! terminal "Installation Commands"
	Depending on how Python is installed on the computer, one of the following commands should allow users to install the software.

	- 
		``` bash
		python3 -m pip install pygpsclient
		```
	- 
		``` bash
		pip install pygpsclient
		```


	??? info "System Requirements"
		This installation method requires an internet connection. Additionally, users will also need administrative privileges *(or root access `sudo`)* for the installation.



### Connecting to the LG290P
Before users can connect to the LG290P GNSS Flex module, they will need to specify the settings of the UART port in PyGPSClient. Once configured, users can select the <kbd>:material-usb:</kbd> button and PyGPSClient will automatically attempt to connect to the GNSS module.

- Below, is a list of the default settings for `UART` ports of the LG290P. These settings should be selected in the configuration menu.
- For the `Serial Port`, select the port associated with the attached USB-to-Serial converter.


<div class="grid" markdown>

<div markdown>

<figure markdown>
[![UART Settings in PyGPSClient](./assets/img/hookup_guide/pygpsclient-uart_settings-small.png){ width="400" }](./assets/img/hookup_guide/pygpsclient-uart_settings-small.png "Click to enlarge")
<figcaption markdown>
Specify the settings for the UART port in QGNSS.
</figcaption>
</figure>

</div>


<div markdown>

!!! info "LG290P - Default Settings"
	The UART ports of the LG290P GNSS module will have the following default configuration:

	- Baudrate: 460800bps
	- Data Bits: 8
	- Parity: No
	- Stop Bits: 1
	- Flow Control: None

</div>

</div>



## Arduino Library
The [SparkFun LG290P Quadband RTK GNSS Arduino Library](https://github.com/sparkfun/SparkFun_LG290P_GNSS_Arduino_Library) can be installed from the library manager in the Arduino IDE by searching for:

	SparkFun LG290P Quadband RTK GNSS Arduino Library

<div class="grid" markdown>

<div markdown>

<figure markdown>
[![](./assets/img/hookup_guide/arduino_library.png "Click to enlarge"){ width="400" }](./assets/img/hookup_guide/arduino_library.png)
<figcaption markdown>
SparkFun LG290P Quadband RTK GNSS Arduino Library in the library manager of the Arduino IDE.
</figcaption>
</figure>

</div>


<div markdown>

!!! tip "Manually Download the Arduino Library"
	For users who would like to manually download and install the library, the `*.zip` file can be accessed from the [GitHub repository](https://github.com/sparkfun/SparkFun_LG290P_GNSS_Arduino_Library) or downloaded by clicking the button below.

	<center>
	[:octicons-download-16:{ .heart } Download the Arduino Library](https://github.com/sparkfun/SparkFun_LG290P_GNSS_Arduino_Library/archive/refs/heads/main.zip){ .md-button .md-button--primary }
	</center>

</div>

</div>
