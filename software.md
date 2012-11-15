---
layout: page
title: Software 
header: Pages
group: navigation
---
{% include JB/setup %}


## 3D Slicer
> Web page: [http://www.slicer.org](http://www.slicer.org)
Slicer, or 3D Slicer, is a free, open source software package for visualization and image analysis. 3D Slicer is natively designed to be available on multiple platforms, including Windows, Linux and Mac Os X. 3D Slicer 3.x and 4.x come with OpenIGTLink interface module, that allows exchanging various data with external software and device. See [documentation for OpenIGTLink IF module for 3D Slicer 4.2](http://www.slicer.org/slicerWiki/index.php/Documentation/4.2/Modules/OpenIGTLinkIF).


## Plus (Public software Library for UltraSound imaging research) 
> Web page: [https://www.assembla.com/spaces/plus/wiki](https://www.assembla.com/spaces/plus/wiki)
Plus is a software package containing library functions and applications for tracked ultrasound image acquisition, calibration, and processing. Features include:

* B-mode and RF acquisition using a wide range of imaging and tracking devices
* Live image and tracking data transfer to 3D Slicer using OpenIGTLink
* Spatial and temporal calibration
* Volume reconstruction

Plus has OpenIGTLink interface that allow you to import those data into other OpenIGTLink-compatible software such as 3D Slicer.

Development of the Plus library is supported by Cancer Care Ontario by funding an Applied Cancer Research Unit at [the Laboratory for Percutaneous Surgery (PerkLab) at Queen's University](http://perk.cs.queensu.ca).


## IGSTK (The Image-Guided Surgery Toolkit)
> Web page: [http://www.igstk.org](http://www.igstk.org)
The Image-Guided Surgery Toolkit is a high-level, component-based framework which provides a common functionality for image-guided surgery applications. The framework is a set of high-level components integrated with low-level open source software libraries and application programming interfaces (API) from hardware vendors.

The cornerstone of IGSTK is robustness. IGSTK provides the following high-level functionality: the ability to read and display medical images, including CT and MRI in DICOM format; an interface to common tracking hardware (e.g., AURORA from NDI); a GUI and visualization capabilities, including four-quadrant view (axial, sagittal, coronal, and 3D) and multi-slice axial view (from 1 x 1 to many by many, such as 10 x 10); point based registration and a means for selecting these points; and robust common internal software services for logging, exception-handling and problem resolution.

IGSTK has OpenIGTLink interface providing connectivity with other OpenIGTLink-compatible software. See [IGSTK Book](http://igstk.org/IGSTK/img/IGSTKTheBookV2.pdf) for more detail.
