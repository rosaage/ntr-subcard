# ntr-subcard
Clone of NTR eeprom subcard

For eeprom/flash selection: https://gbatemp.net/threads/ds-cartridge-replacement-save-chips.646745/

Connector: [Molex SlimStack 2x20 P0.50mm - 53748-0408](https://www.digikey.com/en/products/detail/molex/0537480408/1059857)

# Changes
At least when looking on aliexpress a wide version of U2 is a lot more common and cheap, so I extended the footprint to support `M45PE40-VMW6TG` (4 Mbit Flash) and similar chips.

# Production 512 kbit eeprom
A finished PCB can be ordered from JLCPCB by uploading the `Gerbers.zip` file and checking the PCB Assembly option.
`BOM.csv` and `CPL.csv` will need to be uploaded for the assembly. This is set to use U1 as a 512 kbit eeprom chip, as this version was cheap and in stock at jlcpcb.
By modifiying `BOM.csv` before uploading a different part can be selected (also possible on the website after uploading).
It is also possible to order it with only the connector and passives and solder on U1 or U2 manually.

# Production 2/4 Mbit Flash
I have not looked into a suitable part for U2 from JLCPCB, but I made CPL files for the coordinates for both wide and slim variants:
* Wide 208 mil: `CPL-U2-wide.csv`
* Slim 150 mil: `CPL-U2-slim.csv`

# Finished boards from JLCPCB
![](https://github.com/rosaage/ntr-subcard/blob/main/jlcpcb_finished_boards.jpg)

# Future revisions
While I don't have any plans to make a new revision right now I have some things I would like to add.
By moving the CE pins from flash/eeprom to a SPDT switch and adding a second pull-up it would be possible
to have one card with both eeprom and flash at the same time. A set of solder bridge pads or pads for 0-ohm resistors would also be a quick option if no suitable switch can be sourced.
