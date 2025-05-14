## GNSS Flex System
The GNSS Flex system is designed to be modular with a standardized pin layout that keeps the ecosystem pin-compatible for upgrades and allows boards to be easily swapped for repairs. The ecosystem is comprised of two boards, which mate through two 2x10-pin, 2mm pitch headers.

<figure markdown>
![Utilizing the GNSS Flex System](./assets/img/hookup_guide/animation-attach_module.gif){ width="500" }
<figcaption markdown>Attaching a GNSS Flex module to a GNSS Flex *carrier* board.</figcaption>
</figure>

The SparkPNT GNSS Flex modules function as *plug-in* boards that feature different GNSS receivers. They are designed to mate with *carrier* boards for various purposes; such as a breakout board, Raspberry Pi pHAT, SparkPNT product line, etc.



## Ecosystem Boards
Below are general examples of a GNSS Flex module and *carrier* board.


<!-- Import the component -->
<script type="module" src="https://ajax.googleapis.com/ajax/libs/model-viewer/3.5.0/model-viewer.min.js"></script>

<!-- Material color adjustment (for soldermask) -->
<script type="module" >
	const modelViewer = document.querySelectorAll("model-viewer");
	// To debug in console
	// let material = modelViewer.model.materials;

	for (const iteration of modelViewer) {
		iteration.addEventListener('load', () => {
		const material = iteration.model.materials;
		// material[material.length-1].pbrMetallicRoughness.setBaseColorFactor([224/255, 49/255, 29/255]); //SparkFun Red: #E0311D
		material[material.length-1].pbrMetallicRoughness.setBaseColorFactor([224/255, 0, 0]); // #E00000
		material[material.length-1].pbrMetallicRoughness.setMetallicFactor(.8);
		material[material.length-1].pbrMetallicRoughness.setRoughnessFactor(.7);
		});
	};
</script>


<div class="grid cards" align="center" markdown>

-   **GNSS Flex Module**

	---

	<model-viewer src="../assets/3d_model/GNSS_Flex-Generic_Module.glb" camera-controls poster="../assets/3d_model/poster-generic_module.png" tone-mapping="neutral" shadow-intensity="2" shadow-softness="0.2" camera-orbit="0deg 75deg 0.1623m" field-of-view="25.11deg" style="width: 100%; height: 400px;">
	</model-viewer>


-   **GNSS Flex *"Carrier"* Board**

	---

	<model-viewer src="../assets/3d_model/GNSS_Flex-Carrier_Board.glb" camera-controls poster="../assets/3d_model/poster-carrier_board.png" tone-mapping="neutral" shadow-intensity="2" shadow-softness="0.2" camera-orbit="0deg 75deg 0.1781m" field-of-view="30deg" style="width: 100%; height: 400px;">
	</model-viewer>


</div>


???+ tip "Manipulate 3D Model"
	<center>

	| Controls       | Mouse                    | Touchscreen    |
	| :------------- | :----------------------: | :------------: |
	| Zoom           | Scroll Wheel             | 2-Finger Pinch |
	| Rotate         | ++"Left-Click"++ & Drag  | 1-Finger Drag  |
	| Move/Translate | ++"Right-Click"++ & Drag | 2-Finger Drag  |

	</center>



---



Section Topics
===

This guide is divided into three sections:

- The **Ecosystem Overview** section describes the overall GNSS Flex system and its primary components.
- The **GNSS Flex Modules** and **Carrier Boards** sections detail each of the specific boards in the ecosystem and how they operate.
- In the **Resources and Support** sections, users can find the design files (KiCad files & schematic), relevant documentation (datasheets, white papers, etc.) and other helpful links on the [Resources page](./resources.md). Lastly, the [Troubleshooting page](./troubleshooting_tips.md) includes helpful tips and instructions for how to receive technical support from SparkFun.
