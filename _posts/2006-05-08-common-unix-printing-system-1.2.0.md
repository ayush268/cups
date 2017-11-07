---
title: Common UNIX Printing System 1.2.0
layout: post
permalink: /blog/:year-:month-:day-:title.html
---

<P>CUPS 1.2.0 is now available for download from the CUPS web site at:</P>
- Documentation updates (Issue #1618, Issue #1620, Issue #1622, Issue #1637)
- Static file copy buffers reduced from 64k to 32k to work around bogus MallocDebug library assumptions (Issue #1660)
- The scheduler did not decode the backend exit code properly (Issue #1648)
- The MacOS X USB backend did not report the 1284 device ID, nor did it fix device IDs returned by HP printers.
- The scheduler started more slowly than 1.1.x with large numbers of printers (Issue #1653)
- cupsRasterInterpretPPD() didn't support the cupsPreferredBitsPerColor attribute, and imagetoraster didn't use the new API.
- The "make test" script did not create all of the necessary subdirectories for testing (Issue #1638)
- The scheduler did not prevent rotation of logs redirected to /dev/null (Issue #1651)
- "make test" did not include the SNMP backend in the test environment (Issue #1625)
- The EPM packaging files did not work (Issue #1621)
- "Use Default Configuration" inserted a broken configuration file (Issue #1624)
- Redirects in the web interface did not always preserve the encrypted status of a connection (Issue #1603)
- Added the Apple "pap" backend.
- Added CUPS library to CUPS Image shared library linkage to support Linux --as-needed linker option (Issue #1606)
- Fixed support for --enable-pie (Issue #1609)
- The pdftops filter did not validate the length of the encryption key (Issue #1608)
- Updated the Polish localization.
- "Encryption Required" in the cupsd.conf file now only requires encryption when the connection is not over the loopback interface or domain socket.
- Printer names containing "+" were not quoted properly in the web interface (Issue #1600)
- The SNMP backend now reports the make and model in the information string so that the auto-generated printer name is more useful than just an IP address.