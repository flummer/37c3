# 37c3 NFC Badge by Thomas Flummer

![37c3 badge front and back](https://github.com/flummer/37c3/raw/main/IMAGES/badges_front_back_standing.jpg "37c3 badge front and back")

This is a simple badge, to play a little with NFC using the NXP NTAG I2C Plus chip. There is a PCB antenna coil for the RF interface (can eg. be used for communication with an NFC enabled phone), and there is a StemmaQT/Qwiic compatible connector for I2C communication, often found on many development boards or more advanced badges.

The onboard memory on the NTAG I2C Plus chip is 1K and can hold different data. The badges are preformated for NDEF records and there is a link record on there that includes a link to this repository, but you can change the content, eg. with the NXP TagWriter app for Android or iOS. Be aware that iOS needs the memory to be formatted as NDEF.

You can protect different sections and it is also possible via registers to protect write access to either RF/I2C or BOTH.

**WARNING** If you block access to both interfaces, you will **NOT** be able to change the content on the badge any more.

This badge is heavily inspired with pretty much all the electronics copied from the [BornHack 2023 badge](https://github.com/bornhack/badge2023/) with almosts the same features, though a little bit less memory (the BornHack 2023 version has 2K).

## Designed in KiCad v7

To open the project, you will need to install a recent release version or one of the nightly builds, KiCad v5 or v6 won't open this design.

Main Component:

- [NXP NT3H2111W0FHKH - NTAG I2C plus 1K, NFC Forum Type 2 Tag with I2C interface](https://www.nxp.com/part/NT3H2111W0FHK#/)
    - [datasheet](https://www.nxp.com/docs/en/data-sheet/NT3H2111_2211.pdf)

## License

The hardware design of the `main` branch of this repository is released under the following license:

* the "Creative Commons Attribution-ShareAlike 4.0 International License"
  (CC BY-SA 4.0) full text of this license is included in the LICENSE file
  and a copy can also be found at
  [http://creativecommons.org/licenses/by-sa/4.0/](http://creativecommons.org/licenses/by-sa/4.0/)
