<!-- Import the component -->
<script type="module" src="https://ajax.googleapis.com/ajax/libs/model-viewer/3.5.0/model-viewer.min.js"></script>


## GNSS Flex System
The GNSS Flex system is designed to be modular with a standardized pin layout that keeps the ecosystem pin-compatible for upgrades and allows boards to be easily swapped for repairs. The ecosystem is comprised of two boards, which mate through two 2x10-pin, 2mm pitch headers.


<figure markdown>
<model-viewer alt="Utilizing the GNSS Flex System" src="../assets/3d_model/GNSS_Flex-Stack_Animation.glb" poster="./assets/img/hookup_guide/animation-attach_module.gif" camera-controls autoplay tone-mapping="neutral" shadow-intensity="2" shadow-softness="0.2" camera-orbit="0deg 70deg 16.7m" field-of-view="18deg" camera-target="2.93m 1.16m -1.29m" style="width: 500px; height: 300px;">
</model-viewer>
<figcaption markdown>Attaching a GNSS Flex module to a GNSS Flex *carrier* board.</figcaption>
</figure>


???+ tip "Manipulate 3D Model"
	<article style="text-align: center;" markdown>

	| Controls       | Mouse                    | Touchscreen    |
	| :------------- | :----------------------: | :------------: |
	| Zoom           | Scroll Wheel             | 2-Finger Pinch |
	| Rotate         | ++"Left-Click"++ & Drag  | 1-Finger Drag  |
	| Move/Translate | ++"Right-Click"++ & Drag | 2-Finger Drag  |

	</article>


The SparkPNT GNSS Flex modules function as *plug-in* boards that feature different GNSS receivers. They are designed to mate with *carrier* boards for various purposes; such as a breakout board, Raspberry Pi pHAT, SparkPNT product line, etc.



### Board Variants
Below, are two generic examples of a GNSS Flex *module* and *carrier* board.


<div class="grid cards" align="center" markdown>

-   **GNSS Flex Module**

	---

	<model-viewer src="../assets/3d_model/GNSS_Flex-Generic_Module.glb" camera-controls poster="../assets/3d_model/poster-generic_module.png" tone-mapping="neutral" shadow-intensity="2" shadow-softness="0.2" camera-orbit="0deg 75deg 0.1623m" field-of-view="12deg" style="width: 100%; height: 250px;">
	</model-viewer>

	<article style="text-align: center;" markdown>
	[All GNSS Flex Modules](modules.md){ .md-button .md-button--primary }
	</article>


-   **GNSS Flex *"Carrier"* Board**

	---

	<model-viewer src="../assets/3d_model/GNSS_Flex-Carrier_Board.glb" camera-controls poster="../assets/3d_model/poster-carrier_board.png" tone-mapping="neutral" shadow-intensity="2" shadow-softness="0.2" camera-orbit="0deg 75deg 0.1781m" field-of-view="15deg" style="width: 100%; height: 250px;">
	</model-viewer>

	<article style="text-align: center;" markdown>
	[All GNSS Flex *Carrier* Boards](carriers.md){ .md-button .md-button--primary }
	</article>

</div>



### Ecosystem Boards
Below, are all the available GNSS Flex boards in our ecosystem.

<div class="grid cards" markdown>

--8<-- "./modules.md:9:40"

--8<-- "./carriers.md:9:23"

</div>



---



## Section Topics
This guide is divided into three sections:

- The **Ecosystem Overview** section describes the overall GNSS Flex system and its primary components.
- The **GNSS Flex Modules** and **Carrier Boards** sections detail each of the specific boards in the ecosystem and how they operate.
- In the **Resources and Support** sections, users can find the design files (KiCad files & schematic), relevant documentation (datasheets, white papers, etc.) and other helpful links on the [Resources page](./resources.md). Lastly, the [Troubleshooting page](./troubleshooting_tips.md) includes helpful tips and instructions for how to receive technical support from SparkFun.
