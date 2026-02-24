!!! warning "Need Help?"
	If you need technical assistance or more information on a product that is not working as you expected, we recommend heading on over to the [SparkFun Forums](https://community.sparkfun.com).


	!!! info "Account Registration Required"
		If this is your first visit to our forum, you'll need to create a [Forum Account](https://community.sparkfun.com/signup) to post questions.



## Electrostatic Discharge
The mosaic-G5 P3 GNSS receiver is sensitive to [ESD](https://en.wikipedia.org/wiki/Electrostatic_discharge "Electrostatic Discharge"). Use a proper grounding system to make sure that the working surface and the components are at the same electric potential.

!!! warning "ESD Precaution"
	As recommended by the manufacturer, we highly recommend that users take the necessary precautions to avoid damaging their GNSS receiver.

	<div class="grid cards" markdown>

	<div markdown>

	<article class="video-500px" style="margin: auto;" markdown>
	<iframe src="https://www.youtube.com/embed/hrL5J6Q5gX8?si=jOPBat8rzMnL7Uz4&amp;start=26;&amp;end=35;" title="Septentrio: Getting Started Video (playback starts at ESD warning)" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>

	</div>

	</div>



## GNSS Antenna

### Power Input
!!! danger "Active Antenna"
	Never inject an external DC voltage into the SMA connector for the GNSS antenna, as it may damage the mosaic-G5 P3 GNSS receiver. For instance, when using a splitter to distribute the antenna signal to several GNSS receivers, make sure that no more than one output of the splitter passes DC. Use [DC-blocks](https://en.wikipedia.org/wiki/DC_block) otherwise.



### Supported Frequency Bands
For the best performance, we recommend users choose a compatible L1/L2/L5/L6 GNSS antenna and utilize a low-loss cable. Utilizing an antenna that doesn't match all the supported frequency bands of the mosaic-G5 P3, will result in reduced performance and capabilities.
