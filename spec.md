---
layout: page
title: Specification
header: Pages
group: navigation
---
{% include JB/setup %}

This page is under development. Please refer [OpenIGTLink Protocol Version 2](http://www.na-mic.org/Wiki/index.php/OpenIGTLink/ProtocolV2/Index) for more information.

## OpenIGTLink version 2 Summary
* The header format will not be changed. 
* Simple querying mechanism is defined. See [[OpenIGTLink/ProtocolV2/Query| querying mechanism in version 2]].
* The protocol version 2 continue to focus on message formats. Supporting tools (simulators and interfaces for specific applications e.g. 3D Slicer, Matlab) and transportation layer (use of UDP or other network communication middleware) should be discussed separately.
* More information is available in [[OpenIGTLink/ProtocolV2/Summary| Version 2 Summary page]].

## OpenIGTLink Protocol Rules
* The OpenIGTLink protocol is a network communication protocol works in the Application Layer in the OSI model.
* The minimum unit in data transfer in OpenIGTLink protocol is an ''OpenIGTLink message''.
* An OpenIGTLink message consists of ''header'' and ''body'' sections. The header format is consistent and can be interpreted by all software that has OpenIGTLink interface. The header contains device type (or data type) name, which specifies the format of the body.
* The OpenIGTLink protocol is stateless.

## Architecture and Header 
* [OpenIGTLink Header](protocols/v2_header.html)

## Proposed Message Types
### Message types inherited from version 1
* [TRANSFORM](protocols/v2_transform.html)
* [QTRANS](protocols/v2_qtransform.html) (formerly POSITION)
* [POSITION](protocols/v2_position.html) (alias of QTRANSFORM)
* [IMAGE](protocols/v2_image.html)
* [STATUS](protocols/v2_status)
* [CAPABILITY](protocols/v2_capability)

### New message types for image-guided surgery (IGS) systems
* [IMGMETA](protocols/v2_imagemeta)
* [LBMETA](protocols/v2_labelmeta)
* [COLORT](protocols/v2_colortable)
* [POINT](protocols/v2_point)
* [TRAJ](protocols/v2_trajectory)
* [TDATA](protocols/v2_trackingdata)
* [QTDATA](protocols/v2_qtrackingdata)

### New message types for other applications
* [SENSOR](protocols/v2_sensordata)
* [STRING](protocols/v2_string)
* [NDARRAY](protocols/v2_ndarray)
* [BIND](protocols/v2_bind)
* [POLYDATA](protocols/v2_polydata)

### Other Information
* [64-bit UNIT field in OpenIGTLink](protocols/v2_unit)



