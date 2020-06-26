romhacks
========

This is a personal archive of romhacks

Usage
-----

Unless otherwise specified, the patches will be distributed as ips files.
The patching program, Lunar IPS, will take the the original rom you backed
up and an ips file to produce a new patched rom file.

Steps:

* [Download <link>](https://www.romhacking.net/utilities/240/) and run Lunar IPS
* Ensure your target rom has been extracted from zip
* Select 'Apply patch'
* Follow the title screen in popups - select the ips file, select target rom
* Select where you want to save your patched rom

IPS format
----------

While explaining each is easy enough, ips patch files are very simple to read. There is a
constant `PATCH` ascii in the beginning: `50 41 54 43 48`. Then, multiple hunks follow,
each of which are a 3 byte offset, 2 byte length, and payload. The file ends with EOF `45 4F 46`

[Super Mario Bros. 3](Super_Mario_Bros_3)
===================================================

[Super Riff Bros. 3](Super_Riff_Bros_3)
=================================================

[Super Calm Bros. 3](Super_Calm_Bros_3)
=================================================

License
-------

Please see included LICENSE file for more info