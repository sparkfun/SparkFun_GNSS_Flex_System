## Firmware Update
Users can easily upgrade the firmware for the mosaic-X5 module through its webserver interface. This is useful for updating various features, such as the antenna calibration list.

<article style="text-align: center;" markdown>
![QR code - video](./assets/img/qr_code/video-update_firmware.png){ .qr width="75px" }
</article>

<div class="video-500px" style="margin: auto;">
<iframe src="https://www.youtube.com/embed/bp8kNbzMl_c" title="Septentrio: How to upgrade the firmware of a Septentrio receiver" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>


<div class="grid cards" markdown>

-   To check for the latest firmware published by Septentrio, please visit their [product page](https://www.septentrio.com/en/products/gps/gnss-receiver-modules/mosaic-x5#resources) for the mosaic-X5 module. Users can click on the button below, to be redirected to the latest firmware for the mosaic-X5.

	<article style="text-align: center;" markdown>
	[:septentrio: Find the Latest Firmware](https://www.septentrio.com/en/products/gps/gnss-receiver-modules/mosaic-x5#resources){ .md-button .md-button--primary target="blank" }
	</article>


-   Currently, at the time that this board was released, the firmware for the mosaic-X5 module was *v4.14.10.1*[^4]. Users can download [**version 4.14.10.1**](./assets/component_documentation/firmware/mosaic-X5_fwp_4.14.10.1.zip) of the firmware, by clicking on the button below.

	[^4]:
		For the latest firmware published by Septentrio, please visit their [product page](https://www.septentrio.com/en/products/gps/gnss-receiver-modules/mosaic-x5#resources).<br>
		*This is firmware version, was archived at the time that this guide was written. Please do not request for the file to be updated; instead visit the product page to download the latest firmware.*

	<article style="text-align: center;" markdown>
	[:octicons-download-16:{ .heart } Download Firmware *(v4.14.10.1)*](./assets/component_documentation/firmware/mosaic-X5_fwp_4.14.10.1.zip){ .md-button .md-button--primary target="blank" }
	</article>

</div>


!!! info "Latest Firmware"
	For the latest firmware released by Septentrio, please visit their [product page](https://www.septentrio.com/en/products/gps/gnss-receiver-modules/mosaic-x5#resources) for the mosaic-X5 module.


## Record GNSS Data

<div class="grid" markdown>

<div markdown>

#### Data Logging

This video illustrates how users can configure the settings for data logging to an SD card *(if available)*.


<article style="text-align: center;" markdown>
![QR code - video](./assets/img/qr_code/video-log_data.png){ .qr width="75px" }
</article>


<article class="video-500px" style="margin: auto;">
<iframe src="https://www.youtube.com/embed/Y9tvOebnoxk" title="Septentrio: How to log data to the SD card of the Septentrio mosaic receiver module" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</article>

</div>


<div markdown>

#### Stream Data

This video illustrates how users can configure and enable a data stream for a TCP/IP connection.


<article style="text-align: center;" markdown>
![QR code - video](./assets/img/qr_code/video-data_stream.png){ .qr width="75px" }
</article>


<article class="video-500px" style="margin: auto;">
<iframe src="https://www.youtube.com/embed/ArtePkC58-o" title="Septentrio: How to output NMEA data on the Septentrio mosaic receiver module" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</article>


??? info "Related Video"
	While this instructional video is for a different product line, the information, for the most part, is still relevant.


	<article style="text-align: center;" markdown>
	![QR code - video](./assets/img/qr_code/video-data_stream2.png){ .qr width="75px" }
	</article>


	<article class="video-500px" style="margin: auto;">
	<iframe src="https://www.youtube.com/embed/vU6iwJ-ac6A" title="Septentrio: How to log and stream data in NMEA OR SBF format for GNSS/INS receivers" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>

</div>

</div>

## RTK Corrections

<div class="grid" markdown>

<div markdown>

### IP Server/Client

For users with multiple RTK capable GNSS receivers, users can configure their mosaic-X5 as a rover or base station.


<article style="text-align: center;" markdown>
![QR code - video](./assets/img/qr_code/video-ip_connection.png){ .qr width="75px" }
</article>


<article class="video-500px" style="margin: auto;">
<iframe src="https://www.youtube.com/embed/UVUVXpA8rB4" title="Septentrio: How to receive corrections over an IP connection" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</article>

</div>


<div markdown>

### NTRIP Client

Without having to setup a personal base station, users can receive RTK corrections through the internet from 3rd-party services, like an NTRIP server.


<article style="text-align: center;" markdown>
![QR code - video](./assets/img/qr_code/video-ntrip_connection.png){ .qr width="75px" }
</article>


<article class="video-500px" style="margin: auto;">
<iframe src="https://www.youtube.com/embed/aAPoRpSR0tY" title="Septentrio: How to receive corrections via NTRIP on the Septentrio mosaic receiver module" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</article>


??? example "Polaris RTK"
	The Polaris RTK Corrections Network, provided by PointOne, is an example of a 3rd-party correction service. For users interested in enabling this RTK subscription service, they can check out the [documentation from their website](https://pointonenav.com/news/watch-easy-rtk-setup-for-a-septentrio-mosaic-x5-with-polaris-rtk) and the video below:


	<article style="text-align: center;" markdown>
	![QR code - video](./assets/img/qr_code/video-polaris_rtk.png){ .qr width="75px" }
	</article>


	<article class="video-500px" style="margin: auto;">
	<iframe src="https://www.youtube.com/embed/CPHC-alH0W0" title="Easy RTK setup for a Septentrio Mosaic-X5 with Polaris RTK" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>

</div>

</div>



### Sharing Internet Access
By default, the mosaic-X5 GNSS receiver is not configured to access the internet through the USB interface. In order to receive or cast RTK corrections to/from a RTK network, such as NTRIP, users will need to enable capability.

- Users will need to use the web interface or RxTool software suite to enable the `Outgoing Internet Access Over USB` from the **Communication** > **USB** drop-down menu of the navigation tabs.
- This also requires users to allow Internet sharing through their computer as well. The procedure to do so depends on your operating system.
	- On a Windows PC, users must enable `Allow other network users to connect through this computer's Internet connection`, through the properties option of the network adapter with internet access.
	- On a Linux computer, users will likely need to configure a [network bridge](https://en.wikipedia.org/wiki/Network_bridge).


<article style="text-align: center;" markdown>
![QR code - video](./assets/img/qr_code/video-usb_eth.png){ .qr width="75px" }
</article>


<div class="video-500px" style="margin: auto;">
<iframe src="https://www.youtube.com/embed/bUt8cL9Ue1Y" title="Septentrio: Share internet connection with your GNSS / GPS receiver over USB" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>


!!! info "New IP Address"
	Once a network bridge is enabled, the receiver will receive its IP address from the computer's DHCP server. Depending on the routing table, the module may no longer be reachable at its default IP address *(`192.168.3.1`)*.



## More Videos
Users can find other instructional videos on [Septentrio's YouTube Channel](https://www.youtube.com/channel/UCrA9wMw1y1f-KeOnnhq4lrA/). Feel free to check out their playlists as well:

- [Getting Started](https://www.youtube.com/playlist?list=PLUxLg2_PvvdE0e2i2std6XyPnF6UdecAD)
- [How to *(Videos)* ](https://www.youtube.com/playlist?list=PLUxLg2_PvvdHZ73CnfhS7ZePIIIUR7bON)


??? note "Other Videos"

	<div style="text-align: center;" markdown>
	![QR code - playlist](./assets/img/qr_code/video-playlist.png){ .qr width="150px" }
	</div>

	<div class="grid" markdown>

	<div markdown>

	<article class="video-container" style="margin: auto;">
	<iframe src="https://www.youtube.com/embed/j_zHbl99FsI" title="Septentrio: How to reset a receiver" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>

	</div>


	<div markdown>

	<article class="video-container" style="margin: auto;">
	<iframe src="https://www.youtube.com/embed/D-iqzQnDbWw" title="Septentrio: How to copy the configuration from one to another receiver" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>

	</div>


	<div markdown>

	<article class="video-container" style="margin: auto;">
	<iframe src="https://www.youtube.com/embed/2XizOW3Dzzk" title="Septentrio: How to monitor the CPU of a Septentrio receiver" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>

	</div>


	<div markdown>

	<article class="video-container" style="margin: auto;">
	<iframe src="https://www.youtube.com/embed/9qN6b1JC3uE" title="Septentrio: How to generate and save a diagnostic report of a Septentrio receiver" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>

	</div>


	<div markdown>

	<article class="video-container" style="margin: auto;">
	<iframe src="https://www.youtube.com/embed/WU8MYrDALsE" title="Septentrio: How to log SBF data for support for Septentrio's GNSS/ GPS receivers" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>

	</div>


	<div markdown>

	<article class="video-container" style="margin: auto;">
	<iframe src="https://www.youtube.com/embed/lAP3TXz0ZL8" title="Septentrio: How to set up the PX4 Pixhawk and the Septentrio mosaic-go GNSS receiver Instruction video" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>

	</div>


	<div markdown>

	<article class="video-container" style="margin: auto;">
	<iframe src="https://www.youtube.com/embed/OdGE7bXgJck" title="Septentrio: How to set up ArduPilot with Septentrio AsteRx GNSS receiver + RIB and Pixhawk" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>

	</div>


	<div markdown>

	<article class="video-container" style="margin: auto;">
	<iframe src="https://www.youtube.com/embed/SzI0skGHKEw" title="Septentrio: Anti-jamming feature test-run" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>

	</div>


	<div markdown>

	<article class="video-container" style="margin: auto;">
	<iframe src="https://www.youtube.com/embed/H6uVVEJ5U5w" title="Septentrio: How to activate Wideband Interference Mitigation" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>

	</div>


	<div markdown>

	<article class="video-container" style="margin: auto;">
	<iframe src="https://www.youtube.com/embed/Ib_B_KcfmPs" title="Septentrio: How to use the spectrum plot" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>

	</div>

	</div>
