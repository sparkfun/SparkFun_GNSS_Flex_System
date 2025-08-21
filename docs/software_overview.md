## Manufacturer Software
The software requirements of the GNSS Flex modules are usually specific to the GNSS receiver on the board. Below are general software resources that might be useful; however, users should refer to the **GNSS Flex Modules** section for details on their specific board.


<div class="grid cards" markdown>

- **Septentrio**

	---

	On Windows & Linux platforms, Septentrio provides the RxTools software suite for their GNSS products:

	- [Software Page](https://www.septentrio.com/en/products/gps-gnss-receiver-software/rxtools)
	- [Download & User Manual](https://www.septentrio.com/en/products/gps-gnss-receiver-software/rxtools#resources)
	- [Tutorial Videos](https://www.youtube.com/playlist?list=PLUxLg2_PvvdHZ73CnfhS7ZePIIIUR7bON)


- **Quectel**

	---

	On Windows platforms, Quectel provides the QGNSS *(v2.0)* software application for their GNSS products:

	- [Download & User Manual](https://www.quectel.com/download/qgnss_v2-1_en/)
	- [GitHub Repository](https://github.com/quectel-open-source/GNSSTool)


- **u-blox**

	---

	On Windows platforms, u-blox provides the [u-center 2](https://www.u-blox.com/en/u-center-2) software application for their GNSS products:

	- [Software Page](https://www.u-blox.com/en/product/u-center)
	- [Download](https://u-center2-updates.u-blox.com/u-center2-installer.exe)
	- [User Manual](https://www.u-blox.com/en/info/u-center-2-user-guide)
	- [Webinar](https://www.youtube.com/watch?v=ZYttFyZ_7Uo)
	- [Tutorial Videos](https://www.youtube.com/watch?v=UY2XTb72SXA&list=PLSzSoRUA4EXuo9NTsbTnK84MiKvbVCEKt)

</div>



## Third-Party Software
In addition to any software provided by the manufacturers, there are a variety of third-party software options. The software implementation may even be unique to the available interfaces from an associated *carrier* board.


<div class="grid cards" markdown>

-   **PyGPSClient**

	---

	The `PyGPSClient` Python package is a graphical tool for evaluating the basic performance of GNSS receivers and is compatible with most of the major operating systems. The application parses and extrapolates a variety of data from the UART interface of GNSS receivers; with integrated support for the **NMEA**, **UBX**, **RTCM**, **NTRIP**, and **SPARTN** protocols. All GNSS information is then displayed neatly within its GUI for users to access or utilize.

	- [PyPI - Python Package](https://pypi.org/project/pygpsclient/)
	- [User Manual](https://www.semuconsulting.com/pygpsclient/index.html)
	- [GitHub Repository](https://github.com/semuconsulting/PyGPSClient)

</div>
