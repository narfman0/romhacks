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

Super Mario Bros 3 
==================

All the following patches work for super mario 3 prg0, prg1, and dotsarecool practice
rom. Hashes of original rom files (zips included only for convenience, you still
must extract):

| File name                          | Hash type | Hash                                     |
| ---------------------------------- |:---------:| ----------------------------------------:|
| Super Mario Bros 3 pspeed.nes      | MD5       | 48b16df2b956309d05361d1f2b55152f         |
| Super Mario Bros 3 pspeed.nes      | SHA1      | C24022ACF431DEE19F16915491D82418625D6DB6 |
| Super Mario Bros 3 (U) (PRG 0).zip | MD5       | 19FDA7D7879516017CEFAE7217F8D444         |
| Super Mario Bros 3 (U) (PRG 0).zip | SHA1      | FC249DA7D75070C08EB907F8AC078A13F782635D |
| Super Mario Bros 3 (U) (PRG 0).nes | MD5       | BB5C4B6D4D78C101F94BDB360AF502F3         |
| Super Mario Bros 3 (U) (PRG 0).nes | SHA1      | A03E7E526E79DF222E048AE22214BCA2BC49C449 |

all items
---------

`Super Mario Bros 3 all items.ips` begins all runs with maxed inventory, similar
to debug mode. They ARE single use consumption (another patch should exist later
to permanently enable them).

noauto
------

Remove autoscrollers from the game

nocards
-------

`Super Mario Bros 3 nocards.ips` removes all random card encounters, normally
triggered every time a players score passes a multiple of 80000.

It works by patching around $AC9D. There is a check for coins, and we change
the BCC to immediately RTS (NOP,NOP) instead of whatever branched lameness
normally occurred.

nodeath
-------

`Super Mario Bros 3 nodeath.ips` removes decrement of lives upon enemy death.

nohands
-------

`Super Mario Bros 3 nohands.ips` removes the random hands in world 8 to
give the runner more consistent runs. For practice, a player may still manually
click on the hand to enter a world.

quickdeath
----------

`Super Mario Bros 3 quickdeath.ips` makes Mario's death very quick, so one
may practice and learn much faster, or make a romhack faster to go through.

skip levels
-----------
`Super Mario Bros 3 skip levels.ips` allows for overworld movement over uncompleted
levels.

Note: this is confirmed to work for kamikaze bros 3

License
-------

Please see included LICENSE file for more info