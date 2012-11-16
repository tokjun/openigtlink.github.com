---
layout: page
title: Specification
header: Pages
group: navigation
---
{% include JB/setup %}

This page is under development. Please refer [OpenIGTLink Protocol Version 2](http://www.na-mic.org/Wiki/index.php/OpenIGTLink/ProtocolV2/Index) for more information.

## OpenIGTLink version 2 Summary
*The header format will not be changed. 
*Simple querying mechanism is defined. See [[OpenIGTLink/ProtocolV2/Query| querying mechanism in version 2]].
*The protocol version 2 continue to focus on message formats. Supporting tools (simulators and interfaces for specific applications e.g. 3D Slicer, Matlab) and transportation layer (use of UDP or other network communication middleware) should be discussed separately.
*More information is available in [[OpenIGTLink/ProtocolV2/Summary| Version 2 Summary page]].

## OpenIGTLink Protocol Rules
*The OpenIGTLink protocol is a network communication protocol works in the Application Layer in the OSI model.
*The minimum unit in data transfer in OpenIGTLink protocol is an '''OpenIGTLink message'''.
*An OpenIGTLink message consists of '''header''' and '''body''' sections. The header format is consistent and can be interpreted by all software that has OpenIGTLink interface. The header contains device type (or data type) name, which specifies the format of the body.
*The OpenIGTLink protocol is stateless.

## Architecture and Header 
*[[OpenIGTLink/ProtocolV2/Header| OpenIGTLink Header]]

## Proposed Message Types
### Message types inherited from version 1
* [[OpenIGTLink/ProtocolV2/Type/Transform|TRANSFORM]]
* [[OpenIGTLink/ProtocolV2/Type/QTransform|QTRANS]] (formerly POSITION)
* [[OpenIGTLink/ProtocolV2/Type/Position|POSITION]] (alias of QTRANSFORM)
* [[OpenIGTLink/ProtocolV2/Type/Image|IMAGE]]
* [[OpenIGTLink/ProtocolV2/Type/Status|STATUS]]
* [[OpenIGTLink/ProtocolV2/Type/Capability|CAPABILITY]]

### New message types for image-guided surgery (IGS) systems
* [[OpenIGTLink/ProtocolV2/Type/ImageMeta|IMGMETA]]
* [[OpenIGTLink/ProtocolV2/Type/LabelMeta|LBMETA]]
* [[OpenIGTLink/ProtocolV2/Type/ColorTable|COLORT]]
* [[OpenIGTLink/ProtocolV2/Type/Point|POINT]]
* [[OpenIGTLink/ProtocolV2/Type/Trajectory|TRAJ]]
* [[OpenIGTLink/ProtocolV2/Type/TrackingData|TDATA]]
* [[OpenIGTLink/ProtocolV2/Type/QTrackingData|QTDATA]]

### New message types for other applications
* [OpenIGTLink/ProtocolV2/Type/SensorData|SENSOR]]
* [[OpenIGTLink/ProtocolV2/Type/String|STRING]]
* [[OpenIGTLink/ProtocolV2/Type/NDArray|NDARRAY]]
* [[OpenIGTLink/ProtocolV2/Type/Bind|BIND]]
* [[OpenIGTLink/ProtocolV2/Type/PolyData|POLYDATA]]

### Other Information
* [[OpenIGTLink/ProtocolV2/Unit| 64-bit UNIT field in OpenIGTLink]]


