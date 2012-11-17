---
layout: page
title: Specification > Header
---
{% include JB/setup %}
Back to [Specification](../spec.html)

## Header Structure

    Bytes
    0   2                       14                                      34             42               50              58
    +-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+.....
    | V |          TYPE         |              DEVICE_NAME              |   TIME_STAMP  |   BODY_SIZE   |     CRC64     |   BODY  		  
    +-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+.....

## Byte Order
Big endian should be used for all [numerical values](http://www.opengroup.org/onlinepubs/007908799/xns/htonl.html) (version, body size, crc). Unused spaces are padded with 0 (binary).

## Header Fields

<table border="1" cellpadding="5" cellspacing="0" align="center">
<tr>
<td style="background:#e0e0e0;"> Data
</td><td style="background:#e0e0e0;"> Type
</td><td style="background:#e0e0e0;"> Description
</td></tr>
<tr>
<td align="left"> V
</td><td align="left"> Unsigned short (16bit)
</td><td align="left"> Version number (1)
</td></tr>
<tr>
<td align="left"> TYPE
</td><td align="left"> char[12]
</td><td align="left"> Type name of data
</td></tr>
<tr>
<td align="left"> DEVICE_NAME
</td><td align="left"> char[20]
</td><td align="left"> Unique device name
</td></tr>
<tr>
<td align="left"> TIME_STAMP
</td><td align="left"> 64 bit unsigned int
</td><td align="left"> <a href="/Wiki/index.php/OpenIGTLink/Timestamp" title="OpenIGTLink/Timestamp"> Timestamp</a> or 0 if unused
</td></tr>
<tr>
<td align="left"> BODY_SIZE
</td><td align="left"> 64 bit unsigned int
</td><td align="left"> Size of body in bytes
</td></tr>
<tr>
<td align="left"> CRC
</td><td align="left"> 64 bit unsigned int
</td><td align="left"> 64 bit CRC for body data
</td></tr>
</table>

## Description of Fields
### Version number
### Type name
### Device name
### Time stamp
### Body size
### CRC
The 64-bit CRC used in OpenIGTLink protocol is based on
[hECMA-182 standard](ttp://www.ecma-international.org/publications/files/ECMA-ST/Ecma-182.pdf).
An example code is available in [igtl_util.c](https://github.com/openigtlink/OpenIGTLink/blob/master/Source/igtlutil/igtl_unit.h) in the OpenIGTLink library.

