---
layout: page
title: Specification > Status
header: Pages
---
{% include JB/setup %}

Summary

The STATUS data type is used to notify the receiver about the current status of the sender.
The data consist of status code in a 16-bit unsigned integer, sub code in a 64-bit integer,
error name in a 20-byte-length character string, and a status message. The length of
the status message is determined by the size information in the general header.
The status code is defined as a part of the OpenIGTLink protocol specification listed
bellow. The sub code is device specific and is defined by developers. In addition,
developers can build their own error name/code into the status message and additional
optional description in the following data field.


## Message Types

### STATUS

<table border="1" cellpadding="5" cellspacing="0">
<tr>
<td style="background:#e0e0e0;"> Data
</td><td style="background:#e0e0e0;"> Type
</td><td style="background:#e0e0e0;"> Description
</td></tr>
<tr>
<td align="left"> C
</td><td align="left"> Unsigned short (16bit)
</td><td align="left"> Status code groups: 1-Ok, 2-Generic Error, ... (see below)
</td></tr>
<tr>
<td align="left"> Sub Code
</td><td align="left"> 64 bit integer
</td><td align="left"> Sub code for the error (ex. 0x200 - file not found)
</td></tr>
<tr>
<td align="left"> Error name
</td><td align="left"> char[20]
</td><td align="left"> "Error", "OK", "Warning" - can be anything, don't relay on this
</td></tr>
<tr>
<td align="left"> Status Message (optional)
</td><td align="left"> char[ BodySize - 30 ]
</td><td align="left"> Optional (English) description (ex. "File C:\test.ini not found")
</td></tr>
</table>

### Status codes:

0. Invalid packet - 0 is not used<br />
0. OK (Default status)<br />
0. Unknown error<br />
0. Panic mode (emergency)<br />
0. Not found (file, configuration, device etc)<br />
0. Access denied<br />
0. Busy<br />
0. Time out / Connection lost<br />
0. Overflow / Can't be reached<br />
0. Checksum error<br />
0. Configuration error<br />
0. Not enough resource (memory, storage etc)<br />
0. Illegal/Unknown instruction (or feature not implemented / Unknown command received)<br />
0. Device not ready (starting up)<br />
0. Manual mode (device does not accept commands)<br />
0. Device disabled<br />
0. Device not present<br />
0. Device version not known<br />
0. Hardware failure<br />
0. Exiting / shut down in progress<br />


## GET_STATUS

<table border="1" cellpadding="5" cellspacing="0" align="center">
<tr>
<td style="background:#e0e0e0;"> Data
</td><td style="background:#e0e0e0;"> Type
</td><td style="background:#e0e0e0;"> Description
</td></tr>
</table>

## STT_STATUS

N/A

## STP_STATUS

N/A

## RTS_STATUS

N/A

## Implementations

POSITION type is implemented in the following files:

* [igtlStatusMessage.h](https://github.com/openigtlink/OpenIGTLink/blob/master/Source/igtlStatusMessage.h)
* [igtlStatusMessage.cxx](https://github.com/openigtlink/OpenIGTLink/blob/master/Source/igtlStatusMessage.cxx)

## Contributors

* Junichi Tokuda