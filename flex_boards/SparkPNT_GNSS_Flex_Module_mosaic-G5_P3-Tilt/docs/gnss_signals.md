## Supported GNSS Signals
The mosaic-G5 P3 GNSS receiver is capable of receiving most of the GNSS signals from the various frequency bands of each constellation. By default, the module is only configured to utilize signals (<span style="background-color:green;color:white;">marked in green</span>, in the table below) from specific satellites and frequency bands. Whereas, the <span style="background-color:var(--md-default-fg-color--lighter);">signals marked in grey</span> are also supported by the module, but each signal needs to be enabled before they can be integrated into the computed Position-Velocity-Time (PVT) solution. Meanwhile, any <span style="color:red;">~~signals colored in red and struck out~~</span> are not supported by the mosaic-X5 GNSS receiver; likely due to their proprietary nature, existence outside the module's frequency range, or are experimental/recently implemented.


<article style="text-align: center;" markdown>

<table border="1">

<tr>
	<th align="center" rowspan="2" colspan="2" style="min-width: 3rem;"></th>
	<th align="center" colspan="14">Frequency Band</th>
</tr>

<tr>
	<th align="center">L5/E5</th>
	<th align="center" colspan="6">L2</th>
	<th align="center" colspan="2">L6/E6</th>
	<th align="center" colspan="4">L1/E1</th>
	<th align="center">S</th>
</tr>

<tr>
	<th rowspan="7" class="rotate-cell" style="min-width: 3rem;">
		<div class="rotate-text">GNSS Constellation</div>
	</th>
	<th align="center">GPS</th>
	<td align="center" style="background-color:green;color:white;">L5</td>
	<td align="center" style="background-color:green;color:white;" colspan="2">L2PY</td>
	<td align="center" style="background-color:green;color:white;" colspan="2">L2C</td>
	<td align="center" style="color:red;" colspan="2"><s>L2M</s></td>
	<td align="center" colspan="2"></td>
	<td align="center" style="background-color:green;color:white;">L1CA</td>
	<td align="center" style="color:red;">L1PY</td>
	<td align="center" style="color:red;"><s>L1M</s></td>
	<td align="center" style="background-color:var(--md-default-fg-color--lighter);">L1C</td>
	<td align="center"></td>
</tr>

<tr>
	<th align="center">GLONASS</th>
	<td align="center"></td>
	<td align="center" style="background-color:var(--md-default-fg-color--lighter);" colspan="2">L3</td>
	<td align="center" style="background-color:var(--md-default-fg-color--lighter);" colspan="2">L2P</td>
	<td align="center" style="background-color:green;color:white;" colspan="2">L2CA</td>
	<td align="center" colspan="2"></td>
	<td align="center" style="background-color:green;color:white;" colspan="2">L1CA</td>
	<td align="center" style="color:red;" colspan="2"><s>L1P</s></td>
	<td align="center"></td>
</tr>

<tr>
	<th align="center">Galileo</th>
	<td align="center" style="background-color:green;color:white;">E5a</td>
	<td align="center" style="background-color:green;color:white;" colspan="6">E5b</td>
	<td align="center" style="background-color:var(--md-default-fg-color--lighter);">E6BC</td>
	<td align="center" style="color:red;"><s>E6PRS</s></td>
	<td align="center" style="background-color:green;color:white;" colspan="2">E1BC</td>
	<td align="center" style="color:red;" colspan="2"><s>E1PRS</s></td>
	<td align="center"></td>
</tr>

<tr>
	<th align="center">BeiDou</th>
	<td align="center" style="background-color:green;color:white;">B2a</td>
	<td align="center" style="background-color:var(--md-default-fg-color--lighter);" colspan="3">B2b</td>
	<td align="center" style="background-color:green;color:white;" colspan="3">B2I</td>
	<td align="center" style="background-color:green;color:white;" colspan="2">B3I</td>
	<td align="center" style="background-color:green;color:white;" colspan="2">B1I</td>
	<td align="center" style="background-color:green;color:white;" colspan="2">B1C</td>
	<td align="center"></td>
</tr>

<tr>
	<th align="center">SBAS</th>
	<td align="center" style="background-color:var(--md-default-fg-color--lighter);">L5</td>
	<td align="center" colspan="6"></td>
	<td align="center" colspan="2"></td>
	<td align="center" style="background-color:var(--md-default-fg-color--lighter);" colspan="4">L1</td>
	<td align="center"></td>
</tr>

<tr>
	<th align="center">QZSS</th>
	<td align="center" style="background-color:green;color:white;">L5</td>
	<td align="center" style="background-color:green;color:white;" colspan="6">L2C</td>
	<td align="center" style="background-color:var(--md-default-fg-color--lighter);">L6E/LEX</td>
	<td align="center" style="color:red;"><s>L6D</s></td>
	<td align="center" style="background-color:green;color:white;">L1CA</td>
	<td align="center" style="background-color:var(--md-default-fg-color--lighter);">L1C</td>
	<td align="center" style="background-color:var(--md-default-fg-color--lighter);">L1S/SAIF</td>
	<td align="center" style="color:red;"><s>L1Sb</s></td>
	<td align="center" style="color:red;"><s>S</s></td>
</tr>

<tr>
	<th align="center">NavIC</th>
	<td align="center" style="background-color:var(--md-default-fg-color--lighter);">L5</td>
	<td align="center" colspan="6"></td>
	<td align="center" colspan="2"></td>
	<td align="center" colspan="4"></td>
	<td align="center" style="color:red;"><s>S</s></td>
</tr>

</table>

</article>

!!! info "Legend for GNSS Signals"
	- Supported; <span style="background-color:green;color:white;">Enabled by default</span>
	- Supported; <span style="background-color:var(--md-default-fg-color--lighter);">Not enabled by default</span>
	- <span style="color:red;">~~**Not supported**~~</span>



## Enable Additional Signals
Below, are the commands to configure the mosaic-G5 P3 GNSS receiver to track any of the supported GNSS signals. Additionally, users can also configure whether the signals are utilized in the Position-Velocity-Time (PVT) computations or their navigation data is accessed.


<div class="grid cards" markdown>

-   ### Signal Tracking

	---

	!!! terminal "Command"
		**Enable Trackings of Specific Signals:** `setSignalTracking, <list signals>`


		??? example
			- **List Signals:**
				```
				setSignalTracking, GPSL1CA+GPSL1PY+GPSL2PY+GPSL2C+GPSL5+...
				```
			- **Track All Signals:**
				```
				setSignalTracking,all
				```


-   ### Signal Utilization

	---

	!!! terminal "Command"
		**Enable Use of Specific Signals:** `setSignalUsage, <list signals - PVT>, <list signals - NavData>`


		??? example
			- **List Signals:**
				```
				setSignalUsage, GPSL1CA+GPSL1PY+GPSL2PY+GPSL2C+GPSL5..., GPSL1CA+GPSL1PY+GPSL2PY+GPSL2C+GPSL5...
				```
			- **Use All Signals:**
				```
				setSignalUsage, all, all
				```

</div>


!!! tip
	Don’t forget to save the configuration to boot, if you want the configuration to persist when you cycle power.



## Enable Additional Satellites
Below, are the commands to configure the mosaic-G5 P3 GNSS receiver to utilize additional GNSS satellites that weren't enabled by default. A satellite's tracking and usage must be enabled before their signals can be tracked or utilized.


<div class="grid cards" markdown>

-   ### Satellite Tracking

	---

	!!! terminal "Command"
		**Enable Tracking of Specific Satellites:** `setSatelliteTracking, <list satellites>`


	??? example
		- **List Satellites:**
			```
			setSatelliteTracking, G01+G02+G03+G04+...
			```
		- **Track All Satellites:**
			```
			setSatelliteTracking,all
			```


-   ### Satellite Utilization

	---

	!!! terminal "Command"
		**Enable Use of Specific Satellites:** `setSatelliteUsage, <list satellites>`


	??? example
		- **List Satellites:**
			```
			setSatelliteUsage, G01+G02+G03+G04+...
			```
		- **Use All Satellites:**
			```
			setSatelliteUsage, all
			```

</div>


!!! tip
	Don’t forget to save the configuration to boot, if you want the configuration to persist when you cycle power.



## Enable GPS L5 Signals
Below, are instructions to configure the mosaic-G5 P3 GNSS receiver to utilize the GPS-L5 band.



### Ignore Health Status
Currently, the L5 frequency band from the GPS constellation is pre-operational until a sufficient monitoring capability is established. Therefore, the satellites broadcast an *"unhealthy"* operational status in their L5 signals and prevent its utilization in PVT computations. These commands disable the health masks to allow the L5 band to be tracked and utilized for PVT computations:


!!! terminal "Commands"
	```
	setHealthMask, Tracking, off
	setHealthMask, PVT, off
	```


!!! tip
	Don’t forget to save the configuration to boot, if you want the configuration to persist when you cycle power.



### Enable Signals
Below, are commands enable the tracking and use of the signals from the GPS-L5 band in PVT solutions:


!!! terminal "Commands"
	```
	setSignalTracking, +GPSL5
	setSignalUsage, +GPSL5, +GPSL5
	```


!!! tip
	Don’t forget to save the configuration to boot, if you want the configuration to persist when you cycle power.



### Output Corrections
Below, are the commands for outputting RTK corrections for signals from the GPS-L5 band:


!!! terminal "Command"
	```
	setRTCMv3Formatting, 0, +GPSL5
	```


	!!! warning
		The mosaic-G5 P3 GNSS receiver must be configured to receive those GNSS signals *(see [instructions above](#enable-signals))*; otherwise, it won't have any data to provide the corrections with.


!!! tip
	Don’t forget to save the configuration to boot, if you want the configuration to persist when you cycle power.

