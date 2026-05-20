# captdriver - alternative driver for Canon CAPT printers

This is a fork of https://github.com/mounaiban/captdriver

It focuses on LBP3000 (could have broke support for others) and fixes the following:

* Incorrect paper dimensions
* Slow printing and delay before first print
* Proper error and interal state handling

It is based on my reverse-engineering effors of captmon2 (LBP2900, LBP3000)
and captfilter Linux binaries, and USB data dumps from Windows XP Canon driver,
however all the code has been written by LLM assistant from my documentation,
experiments and observations.

Flaws:
* Does not continue printing after paper jams, no cartridge/opened door — filter terminates, you'll need to reprint manually
* The output is shifted to the left after every page, the printer reports RCF_UNDERRUN, there's a bug somewhere

-------------------------------------------------------------

**Captdriver an alternative driver for Canon laser printers**
that only support the proprietary CAPT communications protocol
and associated data stream formats.

It aims to be a portable and reliable driver that can extend the
service life of existing CAPT-only printers by extending support
to more platforms and newer operating systems.

## Installation and Information

Please check the [Captdriver Wiki](https://github.com/mounaiban/captdriver/wiki)
for a list of [supported devices](https://github.com/mounaiban/captdriver/wiki#supported-devices),
[installation instructions](https://github.com/mounaiban/captdriver/wiki/Building-and-Installing-captdriver%3A-A-Unified-Guide),
project status, technical information and links to more resources.

## Legal Information

Captdriver is Free Software, licensed under the [terms and conditions](https://www.gnu.org/licenses/gpl-3.0.html)
of the [GNU General Public License, Version 3](https://choosealicense.com/licenses/gpl-3.0/)

This is unofficial software not endorsed or authorised by Canon Inc.
and/or its affiliates.
