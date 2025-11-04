<article style="text-align: center;" markdown>
![Banner](./assets/img/banner-hookup_guide.png){ width="650px" }
</article>


## Introduction

<div class="grid cards desc" markdown>

-   <a href="https://www.sparkfun.com/sparkpnt-gnss-flex-module-lg580p.html">
	**SparkPNT GNSS Flex Module - LG580P**<br>
	**SKU:** GPS-28870

	---

	<figure markdown>
	![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/3/0/7/7/1/28870-GNSS-Flex-LG580P-Module-Feature.jpg)
	</figure></a>


	<article style="text-align: center;" markdown>
	![QR code to product page](./assets/img/qr_code/product.png){ .tinyqr }[Purchase from SparkFun :fontawesome-solid-cart-plus:{ .heart }](https://www.sparkfun.com/sparkpnt-gnss-flex-module-lg580p.html){ .md-button .md-button--primary }
	</article>


-   SparkPNT GNSS Flex modules are plug-in boards featuring different GNSS receivers. They are designed to be easily swapped for repairs and pin-compatible for upgrades. The boards have two 2x10-pin, 2mm pitch female headers connecting to carrier boards. For the LG580P GNSS receiver, these pins will break out the USB, UART (x3), and I^2^C* interfaces, along with the PPS and event signals using a standardized pinout.

	This SparkPNT GNSS Flex module is an upgraded version of the [LG290P GNSS Flex module](../SparkPNT_GNSS_Flex_Module_LG290P/index.md). It features the Quectel LG580P quad-band, multi-constellation, high-precision, RTK and heading GNSS receiver with two antenna inputs for instantaneous heading determination down to 0.1&deg;. In traditional navigation systems, such as those used on your phone or car, previous navigation points are utilized to determine the course heading. This is the reason why the arrow indicator will spin or be oriented in the wrong directions when the navigation system first boots or has been stationary for extended periods of time. However, with the LG580 GNSS receiver, users are provided with a dedicated heading without relying on previous course data points, magnetometers/compasses, or gyroscopes in IMUs, which can introduce small errors.

	The LG580P module offers a diverse choice of interfaces including UART, SPI*, I<sup>2</sup>C*, and CAN*. Additionally, the module is capable of simultaneously receiving signals from the `L1`, `L2`, `L5`, and `L6`/`E6` frequency bands of the GPS, GLONASS, Galileo, BDS, QZSS, and NavIC GNSS constellations. In addition, the module supports SBAS augmentation systems (WAAS, EGNOS, BDSBAS, MSAS, GAGAN, KASS, ASECNA, SouthPAN, and SDCM), PPP services* (BDS PPP-B2b, QZSS CLAS, MADOCA-PPP, and Galileo HAS), RTCM, and RTK corrections for precision navigation with a fast convergence time and reliable performance.

	The built-in professional-grade interference signal detection and elimination algorithms, effectively mitigate multiple narrow-band interference sources and significantly improve signal reception performance in complex electromagnetic environments. In addition, the RTK and heading algorithms ensure reliable positioning in challenging scenarios such as urban environments and deep tree cover. With its high-precision, low power consumption and a high positioning and heading update rate of up to 20 Hz, this board is ideal for high-precision navigation applications, such as intelligent robots, precision agriculture, ADAS, and autonomous driving.


	!!! warning "Features Under Development"
		- **I^2^C/SPI/CAN** - Currently, only the UART interface is supported by the module.
		- **PPP Services** - Corrections for some of the PPP services have not been implemented.

</div>


## :material-folder-cog: Design Files

<!-- Import the component -->
<script type="module" src="https://ajax.googleapis.com/ajax/libs/model-viewer/4.0.0/model-viewer.min.js"></script>


<div class="grid cards desc" markdown>

-   :kicad-primary:{ .enlarge-logo } Design Files

	---

	- :fontawesome-solid-file-pdf: [Schematic](./assets/board_files/schematic.pdf)
	- :material-folder-zip: [KiCad Files](./assets/board_files/kicad_files.zip)
	- :material-rotate-3d: [STEP File](./assets/3d_model/cad_model.step)
	- :fontawesome-solid-file-pdf: [Board Dimensions](./assets/board_files/dimensions.pdf):
		- 1.75" x 1.25" (44.45mm x 31.75mm)


-   <!-- Boxes in tabs -->

	=== "3D Model"
		<article style="text-align: center;" markdown>
		<model-viewer src="../assets/3d_model/web_model.glb" camera-controls poster="../assets/3d_model/poster.png" tone-mapping="neutral" shadow-intensity="2" shadow-softness="0.2" camera-orbit="90deg 75deg 0.103m" field-of-view="25.11deg" style="width: 100%; height: 450px;">
		</model-viewer>

		[Download the `*.step` File](./assets/3d_model/cad_model.step "Click to download"){ .md-button .md-button--primary width="250px" }

		</article>


		???+ tip "Manipulate 3D Model"
			<article style="text-align: center;" markdown>

			| Controls       | Mouse                    | Touchscreen    |
			| :------------- | :----------------------: | :------------: |
			| Zoom           | Scroll Wheel             | 2-Finger Pinch |
			| Rotate         | ++"Left-Click"++ & Drag  | 1-Finger Drag  |
			| Move/Translate | ++"Right-Click"++ & Drag | 2-Finger Drag  |

			</article>


	=== "Dimensions"
		<article style="text-align: center;" markdown>
		[![Board Dimensions](./assets/board_files/dimensions.png){ width="450" }](./assets/board_files/dimensions.png "Click to enlarge")
		<figcaption markdown>Dimensions of the LG580P GNSS Flex module.</figcaption>
		</article>


		???+ tip "Need more measurements?"
			For more information about the board's dimensions, users can download the [KiCad files](./assets/board_files/kicad_files.zip) for this board. These files can be opened in KiCad and additional measurements can be made with the measuring tool.


			!!! info ":octicons-download-16:{ .heart } KiCad - Free Download!"
				KiCad is free, open-source [CAD]("computer-aided design") program for electronics. Click on the button below to download their software. *(\*Users can find out more information about KiCad from their [website](https://www.kicad.org/).)*

				<article style="text-align: center;" markdown>
				[Download :kicad-primary:{ .enlarge-logo }](https://www.kicad.org/download/ "Go to downloads page"){ .md-button .md-button--primary width="250px" }
				</article>


			???+ info ":straight_ruler: Measuring Tool"
				This video demonstrates how to utilize the dimensions tool in KiCad, to include additional measurements:

				<article class="video-500px" style="text-align: center; margin: auto;" markdown>
				<iframe src="https://www.youtube.com/embed/-eXuD8pkCYw" title="KiCad Dimension Tool" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
				![QR code to play video](./assets/img/qr_code/dimension_tool.png){ .qr width="85px" }
				</article>

</div>



## Board Layout
The GNSS Flex system is designed around two 2x10-pin, 2mm pitch headers used mate the two types of boards. A standardized pin layout, keeps the ecosystem pin-compatible for upgrades and allows board to be easily swapped for repairs. Depending on the capabilities of the GNSS receiver, these pins will breakout the USB, UART (x4), I^2^C, and SD card interfaces along with any PPS or event signals of the GNSS receiver.

The LG580P GNSS Flex module has the following features:


<div class="grid" markdown>

<div markdown>

<figure markdown>
[![Layout](./assets/img/hookup_guide/layout.png){ width="750" }](./assets/img/hookup_guide/layout.png "Click to enlarge")
<figcaption markdown>Layout of the major components on the LG580P GNSS Flex module.</figcaption>
</figure>

</div>


<div markdown>

1. **LG580P GNSS Receiver**
:	The Quectel LG580P GNSS receiver
1. **GNSS Flex Headers**
:	Two sets of 2x10 pin, 2mm pitch female headers for connecting a GNSS Flex module to *carrier boards*
1. **U.FL Connectors**
:	Two U.FL connectors for attaching external GNSS antennas

</div>

</div>



## LG580P GNSS Receiver
The centerpiece of the LG580P GNSS Flex module, is the [LG580P GNSS receiver](./assets/component_documentation/quectel_lg580p03_hardware_design_v1-0.pdf) from [Quectel](https://www.quectel.com/). The LG580P is a low-power, multi-band, multi-constellation GNSS receiver capable of delivering centimeter-level precision at high update rates. The built-in professional-grade interference signal detection and elimination algorithms, effectively mitigate multiple narrow-band interference sources and significantly improve signal reception performance in complex electromagnetic environments. In addition, the RTK and heading algorithms ensure reliable positioning in challenging scenarios such as urban environments and deep tree cover. With its performance advantages of high-precision and power consumption, this board is an ideal choice for high-precision navigation applications, such as intelligent robots, UAVs, precision agriculture, mining, surveying, and autonomous navigation.


<div class="grid cards" markdown>

<div style="text-align: center;" markdown>

![QR code to product video](./assets/img/qr_code/video-lg580p.png){ .qr width="85px" }

<article class="video-500px" style="margin: auto;" markdown>
<iframe src="https://player.vimeo.com/video/1115089915?h=127c90c2a9" title="Quectel: Product Intro for LG580P GNSS Receiver" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</article>

</div>


-   <figure markdown>
	[![LG580P GNSS receiver](./assets/img/hookup_guide/LG580P.png){ width="300" }](./assets/img/hookup_guide/LG580P.png "Click to enlarge")
	<figcaption markdown>The LG580P module on the LG580P GNSS Flex module.</figcaption>
	</figure>

</div>



<div class="grid" markdown>

<div markdown>

**Features:**

- Supply Voltage: **3.0–3.6V**
- Tracking Channels: 1040
- Concurrent signal reception: 5 + QZSS
	- `L1`, `L2`, `L5`, `E6` frequency bands
- Sensitivity:
	- Acquisition: -145dBm
	- Tracking: -160dBm
	- Reacquisition: -155dBm
- Antenna Power: External
- GNSS Constellations and SBAS Systems:
	- **USA:** GPS + WASS
	- **Russia:** GLONASS + SDCM
	- **EU:** Galileo + EGNOS
	- **China:** BDS + BDSDAS
	- **Japan:** QZSS + MSAS
	- **India:** NavIC + GAGAN
	- **Korea:** KASS
	- **Africa:** ASECNA
	- **Auz/NZ:** SouthPAN
- Accuracy of 1PPS Signal: 5ns
- Update Rate:
	- Default: 10Hz
	- Max: 20Hz

</div>


<div markdown>

<br>

- Time to First Fix *(without AGNSS)*:
	- Cold Start: 28s
	- Warm Start: 28s
	- Hot Start: 1.8s
- RTK Convergence Time: 5s
- Dynamic Performance:
	- Maximum Altitude: 10000m
	- Maximum Velocity: 490m/s
	- Maximum Acceleration: 4g
- Interfaces
	- UART (x3)
		- Baud Rate: 9600–3000000bps
			- **Default:** 460800bps
		- Protocol: `NMEA 0183`/`RTCM 3.x`/`QGC`
	- SPI[^1] (x1)
	- I^2^C[^1] (x1)
	- CAN[^1] (x1)
- Operating temperature: -40&deg;C to +85&deg;C
- Footprint: 21mm × 16mm × 2.7mm
- Weight: 1.4g


</div>

</div>


[^1]:
	!!! warning "Feature Under Development"
		Currently, only the UART interface is supported by the module. Support for the **I^2^C**, **SPI**, and **CAN** interfaces are still under development.



### Power Consumption
The power consumption of the LG580P GNSS receiver depends on the GNSS signals enabled and the positioning mode.

<div class="grid" markdown>

<article style="text-align: center;" markdown>

| Mode        | Power (mW) | Current (mA) |
| :---------- | :--------: | :----------: |
| Acquisition | 323.4      | 98           |
| Tracking    | 382.8      | 116          |
| Backup      | 59.4       | 0.018        |

</article>


<div markdown>

!!! info "Power Modes"

	**Acquisition:**
	:   Module searches for satellites and to determine visible satellites, coarse frequency, and the code phase of satellite signals

	**Tracking:**
	:   Once acquisition is completed, the module tracks satellites and demodulates the navigation data from specific satellites

	**Backup Mode:**
	:   Reduces power consumption. Only backup domain is active and keeps track of time.

</div>

</div>



### Frequency Bands
The LG580P modules are multi-band, multi-constellation GNSS receivers. Below, is a chart illustrating the frequency bands utilized by all the global navigation satellite systems; along with a list of the frequency bands and GNSS systems supported by the LG580P GNSS receiver.


<figure markdown>
[![GNSS frequency bands](https://www.tallysman.com/app/uploads/2021/07/Tallysman-GNSS-Frequencies-v8.0_Chart-1-1024x425.png){ width="800" style="background-color:white"}](https://www.tallysman.com/app/uploads/2021/07/Tallysman-GNSS-Frequencies-v8.0_Chart-1-1024x425.png "Click to enlarge")
<figcaption markdown>Frequency bands of the global navigation satellite systems. (Source: [Tallysman](https://www.tallysman.com/gnss-constellations-radio-frequencies-and-signals/))</figcaption>
</figure>


<div class="grid" markdown>

<div markdown>

**Supported Frequency Bands:**

- GPS: `L1 C/A`, `L5`, `L2C`
- GLONASS: `L1`, `L2`
- Galileo: `E1`, `E5a`, `E5b`, `E6`
- BDS: `B1I`, `B1C`, `B2a`, `B2b`, `B2I`, `B3I`
- QZSS: `L1 C/A`, `L5`, `L2C`, `L6`
- NavIC: `L5`
- SBAS: `L1`
- L-band PPP[^2]:
	- PPP: `B2b`
	- QZSS: `L6`
	- Galileo HAS: `E6`

</div>


<div markdown>

**Supported GNSS Constellations:**

- GPS (USA)
- GLONASS (Russia)
- Galileo (EU)
- BDS (China)
- QZSS (Japan)
- NavIC (India)

**Supported SBAS Systems:**

- WASS (USA)
- SDCM (Russia)
- EGNOS (EU)
- BDSBAS (China)
- MSAS (Japan)
- GAGAN (India)
- KASS (Korea)
- ASECNA (Africa)
- SouthPAN (Aus/NZ)

</div>

</div>


[^2]:
	!!! warning "Feature Under Development"
		Corrections for some of the PPP services have not been implemented.


!!! info
	For a comparison of the frequency bands supported by the LG580P GNSS receivers, refer to sections **1.2**, **1.5**, and **1.6** of the [hardware design manual](./assets/component_documentation/quectel_lg580p03_hardware_design_v1-0.pdf).


??? info "What are Frequency Bands?"
	A [frequency band](https://en.wikipedia.org/wiki/Frequency_band) is a section of the [electromagnetic spectrum](https://en.wikipedia.org/wiki/Electromagnetic_spectrum), usually denoted by the range of its upper and lower limits. In the [radio spectrum](https://en.wikipedia.org/wiki/Radio_spectrum), these frequency bands are usually regulated by region, often through a government entity. This regulation prevents the interference of RF communication; and often includes major penalties for any interference with critical infrastructure systems and emergency services.

	<figure markdown>
	[![GNSS frequency bands](https://gssc.esa.int/navipedia/images/c/cf/GNSS_All_Signals.png){ width="400" }](https://gssc.esa.int/navipedia/images/c/cf/GNSS_All_Signals.png "Click to enlarge")
	<figcaption markdown>Frequency bands of the global navigation satellite systems. (Source: [ESA](https://gssc.esa.int/navipedia/index.php?title=File:GNSS_All_Signals.png "European Space Agency"))</figcaption>
	</figure>

	However, if the various GNSS constellations share similar frequency bands, then how do they avoid interfering with one another? Without going too far into detail, the image above illustrates the frequency bands of each system with a few characteristics specific to their signals. Wit these characteristics in mind, along with other factors, the chart can help users to visualize how multiple GNSS constellations might co-exist with each other.

	For more information, users may find these articles of interest:

	- [GNSS signal](https://gssc.esa.int/navipedia/index.php/GNSS_signal)
	- [GPS Signal Plan](https://gssc.esa.int/navipedia/index.php?title=GPS_Signal_Plan)
	- [GLONASS Signal Plan](https://gssc.esa.int/navipedia/index.php?title=GLONASS_Signal_Plan)
	- [GALILEO Signal Plan](https://gssc.esa.int/navipedia/index.php?title=GALILEO_Signal_Plan)



### Position Accuracy

<div class="grid" markdown>

<div markdown>

The accuracy of the position reported from the LG580P GNSS receiver, can be improved based upon the correction method being employed. Currently, [RTK](https://en.wikipedia.org/wiki/Real-time_kinematic_positioning "Real-Time Kinematic") corrections provide the highest level of accuracy; however, users should be aware of certain limitations of the system:

- RTK technique requires real-time correction data from a reference station or network of base stations.
	- RTK corrections usually come from RTCM messages that are signal specific *(i.e. an RTK network may only provide corrections for specific signals; only `E5b` and not `E5a`)*.
- The range of the base stations will vary based upon the method used to transmit the correction data.
- The reliability of RTK corrections are inherently reduced in [multipath environments](https://en.wikipedia.org/wiki/Multipath_propagation).

</div>


<div markdown>

<article style="text-align: center;" markdown>

| Correction Method                                                                             | Horizontal                   | Vertical                 | Heading  | Velocity                                |
| :-------------------------------------------------------------------------------------------- | :--------------------------: | :----------------------: | :------: | :-------------------------------------: |
| Standalone                                                                                    | 1.0m<br>~3.3'                | 1.5m<br>~4.9'            |          | 3cm/s (0.108kph)<br>~1.2in/s (0.067mph) |
| [RTK](https://en.wikipedia.org/wiki/Real-time_kinematic_positioning "Real-Time Kinematic")    | **0.8cm** *(+1ppm)*<br>~0.3" | 1.5cm *(+1ppm)*<br>~0.6" | 0.1&deg; |                                         |

</article>

</div>

</div>


??? info "RTK Corrections"
	To understand how RTK works, users will need a more fundamental understanding of the signal error sources.

	<div class="grid cards" markdown align="center">

	-   <a href="https://www.sparkfun.com/news/7533">
		<figure markdown>
		![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/home_page_posts/7/5/3/3/rtk-blog-thumb.png)
		</figure>

		---

		**Real-Time Kinematics Explained**</a>


	-   <a href="https://www.sparkfun.com/news/7138">
		<figure markdown>
		![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/home_page_posts/7/1/3/8/SparkFun_RTK_Facet_-_Surveying_Monopod.jpg)
		</figure>

		---

		**What is Correction Data?**</a>


	-   <a href="https://www.septentrio.com/en/learn-more/insights/gnss-corrections-demystified">
		<figure markdown>
		![Tutorial Thumbnail](https://www.septentrio.com/sites/default/files/styles/blog_picture_v2/public/blog/Septentrio-GNSS-corrections-map-world-web.png)
		</figure>

		---

		**GNSS Corrections Demystified**</a>

	</div>


!!! tip
	For the best performance, we highly recommend that users configure the module to utilize/provide RTK corrections with a compatible L1/L2/L5/L6 GNSS antenna and utilize a low-loss cable.



## GNSS Flex Headers
The GNSS Flex system is designed around two 2x10-pin, 2mm pitch headers used mate the two types of boards. A standardized pin layout, keeps the ecosystem pin-compatible for upgrades and allows boards to be easily swapped for repairs. For the LG580P GNSS receiver, these pins will breakout the UART interface along with three of the programmable I/O pins; the LNA enable pin is not broken out and the safe-boot pin is only exposed as a test point on this board.


<div class="grid" markdown>

<div markdown>

<figure markdown>
[![Peripherals and I/O pins](./assets/img/hookup_guide/pinout-full.png){ width="400" }](./assets/img/hookup_guide/pinout-full.png "Click to enlarge")
<figcaption markdown>The peripherals and I/O pins on the LG580P GNSS Flex module.</figcaption>
</figure>

</div>


<div markdown>
Below, are the features that are available from the LG580P GNSS receiver.

**Supported Interfaces:**

- UART (x3)
- ~~SPI[^1]~~
- ~~I^2^C[^1]~~
- ~~CAN[^1]~~
- ~~Event Trigger[^3]~~
- PPS Signal
- RTK Signal
- Module Reset

[^3]:
	!!! warning "Feature Under Development"
		The event trigger has not been implemented.

</div>

</div>



=== "UART Ports"
	The LG580P GNSS receiver has three UART ports, which can be operated and configured separately.

	<div class="grid" markdown>

	<div markdown>

	<figure markdown>
	[![UART interface](./assets/img/hookup_guide/headers-uart.png){ width="400" }](./assets/img/hookup_guide/headers-uart.png "Click to enlarge")
	<figcaption markdown>The UART ports on the LG580P GNSS Flex module.</figcaption>
	</figure>

	</div>


	<div markdown>

	!!! info "UART Settings"
		The UART ports have the following configuration settings:

		- Logic Level: **3.3V**
		- Baudrate: 9600bps, 115200bps, 230400bps, 460800bps, 921600bps, and 3000000bps 
		- Data Bits: 8
		- Parity: No
		- Stop Bits: 1
		- Flow Control: N/A
		- Supported Protocols:
			- `NMEA 0183` (`PQTM`)
			- `RTCM 3.x`
			- `QGC`


		??? note "Additional Support"
			All of the UART ports support firmware updates through their interface. In addition, the `UART1` port also supports debugging data and the `UART3` interface can be multiplexed for the CAN bus interface[^1].

	</div>

	</div>


	??? info "UART Protocols"
		#### UART Protocols
		By default, these UART ports are configured to transmit and receive `NMEA 0183`, `RTCM 3.x`, and/or `QGC` messages. These messages are generally used for transmitting PNT data; providing or receiving RTK corrections; and receiving PPP data, respectively. Quectel also implements a system of proprietary messages (`PQTM`) for users to configure the LG580P that follows a data format similar to the `NMEA` protocol. The expected structure of these proprietary messages is shown below:


		<div class="grid" markdown>

		<div markdown>

		<figure markdown>
		[![NMEA data structure](./assets/img/hookup_guide/nmea_protocol.png){ width="600" }](./assets/img/hookup_guide/nmea_protocol.png "Click to enlarge")
		<figcaption markdown>The data structure of Quectel messages for the `NMEA` and `PQTM` protocols.</figcaption>
		</figure>

		</div>


		<div markdown>

		<figure markdown>
		[![QGC data structure](./assets/img/hookup_guide/qgc_protocol.png){ width="600" }](./assets/img/hookup_guide/qgc_protocol.png "Click to enlarge")
		<figcaption markdown>The data structure of Quectel messages for the `QGC` protocol.</figcaption>
		</figure>

		</div>

		</div>


		=== "NMEA"
			A full list of compatible `NMEA 0183` v4.11 messages, is provided in section **2.2. Standard Messages** of the [GNSS Protocol Specification](./assets/component_documentation/quectel_lg290p03lgx80p03_gnss_protocol_specification_v1-1.pdf) manual. This protocol is used for outputting GNSS data, as detailed by the [National Marine Electronics Association](https://www.nmea.org/) organization.


			??? abstract "List of Standard NMEA Messages"
				<article style="text-align: center;" markdown>

				| Message | Type Mode | Message Description               |
				| :-----: | :-------: | :-------------------------------- |
				| RMC | Output | Recommended Minimum Specific GNSS Data   |
				| GGA | Output | Global Positioning System Fix Data       |
				| GSV | Output | GNSS Satellites in View                  |
				| GSA | Output | GNSS DOP and Active Satellites           |
				| VTG | Output | Course Over Ground & Ground Speed        |
				| GLL | Output | Geographic Position – Latitude/Longitude |
				| GBS | Output | GNSS Satellite Fault Detection           |
				| GNS | Output | GNSS Fix Data                            |
				| GST | Output | GNSS Pseudorange Error Statistics        |
				| ZDA | Output | UTC Time & Date                          |
				| HDT | Output | True Vessel Heading                      |
				| THS | Output | True, Heading, and Status                |

				</article>


		=== "PQTM"
			A full list of PQTM messages (proprietary NMEA messages defined by Quectel) supported by LG580P, is provided in section **2.3. PQTM Messages** of the [GNSS Protocol Specification](./assets/component_documentation/quectel_lg290p03lgx80p03_gnss_protocol_specification_v1-1.pdf) manual. This protocol is used to configure or read the settings for the LG580P GNSS receiver.


			??? abstract "List of Proprietary Quectel Messages"
				<article style="text-align: center;" markdown>

				| Message            | Type Mode    | Message Description                              |
				| :----------------- | :----------: | :----------------------------------------------- |
				| PQTMVER            | Output       | Outputs the firmware version                     |
				| PQTMCOLD           | Command      | Performs a cold start                            |
				| PQTMWARM           | Command      | Performs a warm start                            |
				| PQTMHOT            | Command      | Performs a hot start                             |
				| PQTMSRR            | Command      | Performs a system reset and reboots the receiver |
				| PQTMUNIQID         | Command      | Queries the module unique ID                     |
				| PQTMSAVEPAR        | Command      | Saves the configurations into NVM                |
				| PQTMRESTOREPAR     | Command      | Restores the parameters configured by all commands to their default values |
				| PQTMVERNO          | Command      | Queries the firmware version                     |
				| PQTMCFGUART        | Set/Get      | Sets/gets the UART interface                     |
				| PQTMCFGPPS         | Set/Get      | Sets/gets the PPS feature                        |
				| PQTMCFGPROT        | Set/Get      | Sets/gets the input and output protocol for a specified port |
				| PQTMCFGNMEADP      | Set/Get      | Sets/gets the decimal places of standard NMEA messages |
				| PQTMEPE            | Output       | Outputs the estimated position error             |
				| PQTMCFGMSGRATE     | Set/Get      | Sets/gets the message output rate on the current interface |
				| PQTMVEL            | Output       | Outputs the velocity information                 |
				| PQTMCFGGEOFENCE    | Set/Get      | Sets/gets geofence feature                       |
				| PQTMGEOFENCESTATUS | Output       | Outputs the geofence status                      |
				| PQTMGNSSSTART      | Command      | Starts GNSS engine                               |
				| PQTMGNSSSTOP       | Command      | Stops GNSS engine                                |
				| PQTMTXT            | Output       | Outputs short text messages                      |
				| PQTMCFGSVIN        | Set/Get      | Sets/gets the Survey-in feature                  |
				| PQTMSVINSTATUS     | Output       | Outputs the Survey-in status                     |
				| PQTMPVT            | Output       | Outputs the PVT (GNSS only) result               |
				| PQTMCFGRCVRMODE    | Set/Get      | Sets/gets the receiver working mode              |
				| PQTMDEBUGON        | Command      | Enables debug log output                         |
				| PQTMDEBUGOFF       | Command      | Disables debug log output                        |
				| PQTMCFGFIXRATE     | Set/Get      | Sets/gets the fix interval                       |
				| PQTMCFGRTK         | Set/Get      | Sets/gets the RTK mode                           |
				| PQTMCFGCNST        | Set/Get      | Sets/gets the constellation configuration        |
				| PQTMDOP            | Output       | Outputs dilution of precision                    |
				| PQTMPL             | Output       | Outputs protection level information             |
				| PQTMCFGODO         | Set/Get      | Sets/gets the odometer feature                   |
				| PQTMRESETODO       | Command      | Resets the accumulated distance recorded by the odometer |
				| PQTMODO            | Output       | Outputs the odometer information                 |
				| PQTMCFGSIGNAL      | Set/Get      | Sets/gets GNSS signal mask                       |
				| PQTMCFGSAT         | Set/Get      | Sets/gets GNSS satellite mask                    |
				| PQTMCFGRSID        | Set/Get      | Sets/gets the reference station ID               |
				| PQTMCFGRTCM        | Set/Get      | Sets/gets RTCM                                   |
				| PQTMCFGSBAS        | Set/Get      | Configures SBAS                                  |
				| PQTMCFGNMEATID     | Set/Get      | Configures the NMEA Talker ID                    |
				| PQTMTAR            | Output       | Outputs the time and attitude                    |
				| PQTMCFGBLD         | Set/Get      | Configures the baseline distance                 |
				| PQTMCFGRTKSRCTYPE  | Set/Get      | Configures RTK differential source type          |
				| PQTMSN             | Command      | Reads the SN of module                           |
				| PQTMCFGANTINF      | Set/Get      | Configures the antenna information               |
				| PQTMCFGANTDELTA    | Set/Get      | Configures the delta between antennas            |
				| PQTMCFGSIGGRP      | Set/Get      | Configures the GNSS signal group                 |
				| PQTMCFGSIGNAL2     | Set/Get      | Configures GNSS signal mask for second antenna   |
				| PQTMCFGGEOSEP      | Set/Get      | Configures geoidal separation                    |
				| PQTMCFGCNRTHD      | Set/Get      | Configures the CNR threshold for position engine |
				| PQTMCFGELETHD      | Set/Get      | Configures the elevation threshold for position engine |
				| PQTMNAV            | Output       | Outputs the navigation information               |
				| PQTMEOE            | Output       | Outputs the end of epoch information             |
				| PQTMCFGWN          | Set/Get      | Configures the reference start week number       |
				| PQTMANTENNASTATUS  | Output       | Reports the antenna status                       |

				</article>


		=== "QGC"
			A full list of QGC messages (proprietary protocol defined by Quectel) supported by LG580P, is provided in section **3. QGC Protocol** of the [GNSS Protocol Specification](./assets/component_documentation/quectel_lg290p03lgx80p03_gnss_protocol_specification_v1-1.pdf) manual. This protocol is used to output the PPP raw data.

			??? abstract "List of Proprietary Quectel Messages"
				<article style="text-align: center;" markdown>

				| GQC Message Name | Message Group | Message Number | Type | Description |
				| :--------- | :--: | :--: | :----: | :--------------------------------- |
				| RAW-PPPB2B | 0x0A | 0xB2 | Output | BDS PPPB2B binary raw messages     |
				| RAW-QZSSL6 | 0x0A | 0xB6 | Output | QZSSL6 binary raw messages         |
				| RAW-HASE6  | 0x0A | 0xE6 | Output | Galileo HASE6 binary raw messages  |

				</article>


		=== "RTCM"
			A full list of compatible `RTCM v3` messages, is provided in section **4. RTCM Protocol** of the [GNSS Protocol Specification](./assets/component_documentation/quectel_lg290p03lgx80p03_gnss_protocol_specification_v1-1.pdf) manual. This protocol is used for transferring GNSS raw measurement data, as detailed by the [Radio Technical Commission for Maritime Services](https://www.rtcm.org/) organization.


			??? abstract "List of Supported RTCMv3 *(MSM)* Messages"
				<article style="text-align: center;" markdown>

				| Message | Type Mode | Message Description                              |
				| :--: | :----------: | :----------------------------------------------- |
				| 1005 | Input/Output | Stationary RTK Reference Station ARP             |
				| 1006 | Input/Output | Stationary RTK Reference Station ARP with height |
				| 1019 | Input/Output | GPS Ephemerides                                  |
				| 1020 | Input/Output | GLONASS Ephemerides                              |
				| 1041 | Input/Output | NavIC/IRNSS Ephemerides                          |
				| 1042 | Input/Output | BDS Satellite Ephemeris Data                     |
				| 1044 | Input/Output | QZSS Ephemerides                                 |
				| 1046 | Input/Output | Galileo I/NAV Satellite Ephemeris Data           |
				| 1073 | Input/Output | GPS MSM3 |
				| 1074 | Input/Output | GPS MSM4 |
				| 1075 | Input/Output | GPS MSM5 |
				| 1076 | Input/Output | GPS MSM6 |
				| 1077 | Input/Output | GPS MSM7 |
				| 1083 | Input/Output | GLONASS MSM3 |
				| 1084 | Input/Output | GLONASS MSM4 |
				| 1085 | Input/Output | GLONASS MSM5 |
				| 1086 | Input/Output | GLONASS MSM6 |
				| 1087 | Input/Output | GLONASS MSM7 |
				| 1093 | Input/Output | Galileo MSM3 |
				| 1094 | Input/Output | Galileo MSM4 |
				| 1095 | Input/Output | Galileo MSM5 |
				| 1096 | Input/Output | Galileo MSM6 |
				| 1097 | Input/Output | Galileo MSM7 |
				| 1113 | Input/Output | QZSS MSM3 |
				| 1114 | Input/Output | QZSS MSM4 |
				| 1115 | Input/Output | QZSS MSM5 |
				| 1116 | Input/Output | QZSS MSM6 |
				| 1117 | Input/Output | QZSS MSM7 |
				| 1123 | Input/Output | BDS MSM3 |
				| 1124 | Input/Output | BDS MSM4 |
				| 1125 | Input/Output | BDS MSM5 |
				| 1126 | Input/Output | BDS MSM6 |
				| 1127 | Input/Output | BDS MSM7 |
				| 1133 | Input/Output | NavIC/IRNSS MSM3 |
				| 1134 | Input/Output | NavIC/IRNSS MSM4 |
				| 1135 | Input/Output | NavIC/IRNSS MSM5 |
				| 1136 | Input/Output | NavIC/IRNSS MSM6 |
				| 1137 | Input/Output | NavIC/IRNSS MSM7 |

				</article>



=== "PPS Output"
	From the module, the [PPS](https://en.wikipedia.org/wiki/Pulse-per-second_signal "Pulse Per Second") output signal is a 3.3V signal output.


	<figure markdown>
	[![I/O for PPS signal](./assets/img/hookup_guide/headers-pps.png){ width="400" }](./assets/img/hookup_guide/headers-pps.png "Click to enlarge")
	<figcaption markdown>The `PPS` signal's output on the LG580P GNSS Flex module.</figcaption>
	</figure>


	!!! tip "Use Case"
		- Users could use this signal in conjunction with the event pins to synchronize two modules with each other.
		- Users could use this signal to create their own **Stratum 0** source for the [NTP](https://en.wikipedia.org/wiki/Network_Time_Protocol "Network Time Protocol") on a primary time server.



=== "LED Output"
	The `RTK` pin operates as the `RTK_STAT` status indicator for the [RTK](https://en.wikipedia.org/wiki/Real-time_kinematic_positioning "Real-Time Kinematic") positioning.


	<figure markdown>
	[![I/O for RTK signal](./assets/img/hookup_guide/headers-led.png){ width="400" }](./assets/img/hookup_guide/headers-led.png "Click to enlarge")
	<figcaption markdown>The `RTK_LED` pin on the LG580P GNSS Flex module.</figcaption>
	</figure>


	!!! info
		The `RTK_STAT` pin is used to indicate [RTK](https://en.wikipedia.org/wiki/Real-time_kinematic_positioning "Real-Time Kinematic") status. The pin is at high level during startup.

		1. If the pin output is high, it indicates the module has entered the RTK fixed mode.
		2. If the pin output is low, it indicates that the module exited the RTK fixed mode or is in backup mode.
		3. If the pin outputs an alternating pin level, it indicates that the module received the correct RTCM data and did not enter the RTK fixed mode. The default frequency is 10Hz.



=== "Event Trigger"
	This pin can be triggered by inputs with an adjustable frequency and polarity.

	<figure markdown>
	[![Event trigger](./assets/img/hookup_guide/headers-event.png){ width="400" }](./assets/img/hookup_guide/headers-event.png "Click to enlarge")
	<figcaption markdown>The event pin on the LG580P GNSS Flex module.</figcaption>
	</figure>


	!!! tip "Use Case"
		Users could use this pin in conjunction with the PPS signal to synchronize two modules with each other.



=== "Reset"
	This pin can be used to reset the LG580P module if it enters an abnormal state. To reset the GNSS receiver, the pin must be low for more than 100ms.


	<figure markdown>
	[![Reset](./assets/img/hookup_guide/headers-reset.png){ width="400" }](./assets/img/hookup_guide/headers-reset.png "Click to enlarge")
	<figcaption markdown>The reset pin on the LG580P GNSS Flex module.</figcaption>
	</figure>


## U.FL Connectors
Users will need to connect compatible GNSS antennas to the `Primary Antenna` and `Secondary Antenna` U.FL connectors. The type of antenna used with the LG580P module affects the overall accuracy of the position and attitude calculated by the GNSS receiver.

- Passive antennas are not recommended for the LG580P GNSS receiver.
- To mitigate the impact of out-of-band signals, utilize an active antenna whose SAW filter is placed in front of the LNA in the internal framework.
	- **DO NOT** select an antenna with the LNA placed in the front.
- There is no need to inject an external DC voltage for the GNSS antenna. Power is already provided from the LG580P module for the LNA of an active antenna.


<figure markdown>
[![GNSS antenna inputs](./assets/img/hookup_guide/ant.png){ width="400" }](./assets/img/hookup_guide/ant.png "Click to enlarge")
<figcaption markdown>The U.FL connectors to attach external GNSS antennas to the LG580P GNSS Flex module.</figcaption>
</figure>


!!! tip
	For the best performance, we recommend users choose compatible L1/L2/L5/L6/L-Band GNSS antennas and utilize a low-loss cables. Also, don't forget that GNSS signals are fairly weak and can't penetrate buildings or dense vegetation. The GNSS antennas should have an unobstructed view of the sky.
