<show-structure depth="2"/>

# AUMT Standardised Components

In order to reduce the number of components we need to keep around and
reduce the costs of producing PCBs, some common components have been standardised between boards.
This means that anytime you are designing a board, these components should be your first choice and
others should only be used if you have a very good reason to do so.

## Passives

<tldr>
    TLDR: Use E6 for capacitors and E12 for resistors. Everything should be 0805.
</tldr>

All resistors and capacitors should be 0805 (imperial) in size. This has been found to provide a good balance
between the footprint size and hand-solderability.

In order to reduce the number of resistors we need to order, the team has adopted the industry
practice of using the E-series of preferred values (see
more <a href="https://en.wikipedia.org/wiki/E_series_of_preferred_numbers">here</a>). 
More specifically we use the E12 line of values for resistors and the E6 for capacitors. 


For resistors, in the very rare situation you need a different value outside of E12, try to stick to the E24 values. 
The most common situation where this will occur is when you need a specific voltage divider. Some common ones we use
13.3V to 5V, 13.3V to 3.3V and 5V to 3.3V. The resistor combinations for these are listed below:

- 12V to 5V -> 10k and 6k
- 12V to 3.3V -> 10k and 3.3k
- 5V to 3.3V -> 10k and 20k

<tabs>
    <tab title="E6">
        <list>
            <li> 1.0pF, 1.5pF, 2.2pF, 3.3pF, 4.7pF, 6.8pF </li>
            <li> 10pF, 15pF, 22pF, 33pF, 47pF, 68pF </li>
            <li> 100pF, 150pF, 220pF, 330pF, 470pF, 680pF </li>
            <li> 1nF, 1.5nF, 2.2nF, 3.3nF, 4.7nF, 6.8nF </li>
            <li> 10nF, 15nF, 22nF, 33nF, 47nF, 68nF </li>
            <li> 100nF, 150nF, 220nF, 330nF, 470nF, 680nF </li>
            <li> 1μF, 1.5μF, 2.2μF, 3.3μF, 4.7μF, 6.8μF </li>
            <li> 10μF, 15μF, 22 μF, 33μF, 47μF, 68μF </li>
            <li> 100μF, 150μF, 220μF, 330μF, 470μF, 680μF </li>
            <li> 1000μF, 1500μF, 2200μF, 3300μF, 4700μF, 6800μF </li>
            <li> 10000μF </li>
        </list>
    </tab>
    <tab title="E12">
        <list>
            <li> 1.0, 1.2, 1.5, 1.8, 2.2, 2.7, 3.3, 3.9, 4.7, 5.6, 6.8, 8.2 </li>
            <li> 10, 12, 15, 18, 22, 27, 33, 39, 47, 56, 68, 82 </li>
            <li> 100, 120, 150, 180, 220, 270, 330, 390, 470, 560, 680, 820 </li>
            <li> 1k, 1.2k, 1.5k, 1.8k, 2.2k, 2.7k, 3.3k, 3.9k, 4.7k, 5.6k, 6.8k, 8.2k </li>
            <li> 10k, 12k, 15k, 18k, 22k, 27k, 33k, 39k, 47k, 56k, 68k, 82k </li>
            <li> 100k, 120k, 150k, 180k, 220k, 270k, 330k, 390k, 470k, 560k, 680k, 820k </li>
            <li> 1M, 1.2M, 1.5M, 1.8M, 2.2M, 2.7M, 3.3M, 3.9M, 4.7M, 5.6M, 6.8M, 8.2M </li>
            <li> 10M </li>
        </list>
    </tab>
    <tab title="E24">
        <list>
            <li> 1.0, 1.1, 1.2, 1.3, 1.5, 1.6, 1.8, 2.0, 2.2, 2.4, 2.7, 3.0, 3.3, 3.6, 3.9, 4.3, 4.7, 5.1, 5.6, 6.2, 6.8, 7.5, 8.2, 9.1 </li>
            <li> 10, 11, 12, 13, 15, 16, 18, 20, 22, 24, 27, 30, 33, 36, 39, 43, 47, 51, 56, 62 68, 75, 82, 91 </li>
            <li> 1k, 1.1k, 1.2k, 1.3k, 1.5k, 1.6k, 1.8k, 2.0k, 2.2k, 2.4k, 2.7k, 3.0k, 3.3k, 3.6k, 3.9k, 4.3k, 4.7k, 5.1k, 5.6k, 6.2k, 6.8k, 7.5k, 8.2k, 9.1k </li> 
            <li> 10k, 11k, 12k, 13k, 15k, 16k, 18k, 20k, 22k, 24k, 27k, 30k, 33k, 36k, 39k, 43k, 47k, 51k, 56k, 62k, 68k, 75k, 82k, 91k </li>
            <li> 100k, 110k, 120k, 130k, 150k, 160k, 180k, 200k, 220k, 240k, 270k, 300k, 330k, 360k, 390k, 430k, 470k, 510k, 560k, 620k, 680k, 750k, 820k, 910k </li>
            <li> 1M, 1.1M, 1.2M, 1.3M, 1.5M, 1.6M, 1.8M, 2.0M, 2.2M, 2.4M, 2.7M, 3.0M, 3.3M, 3.6M, 3.9M, 4.3M, 4.7M, 5.1M, 5.6M, 6.2M, 6.8M, 7.5M, 8.2M, 9.1M </li>
            <li> 10M</li>
        </list>
    </tab>
</tabs>

## LEDs

LEDs are great visual indicators and should be used on boards to provide a visual indication of what's happening.
If possible and LED should be connected to a pin on the MCU of the board to act as a debug LED and provide an easy way
to ensure the MCU is working after assembly. They also should be placed on the voltage rail to provide a visual indicator
that there is voltage being fed to the board and that the regulators are working correctly. 

All LEDs should be 0805 (imperial) in size for the same reasons outlined above.

Red LEDs should be used to indicate errors, while green LEDs should be used to indicate an OK status. Other LEDs
(such as the status LED) should be blue in colour. 

## Voltage Regulators

<warning> When designing for voltage regulators ensure you know the current requirements of your circuit and do the 
appropriate thermal calculations to ensure you do not exceed the maximum recommended junction temperature! </warning>

<tip> The TI datasheet (found <a href="https://www.ti.com/lit/ds/symlink/lm1117.pdf">here</a> ) is a great resource for the thermal
calculations required. </tip>

Voltage regulators are an essential part of basically any PCB, and as such we do not want to be using 10 different. 
The LM1117 series is an extremely common <u>L</u>ow <u>D</u>rop<u>o</u>ut (LDO) regulator with both adjustable and fixed
(1.8V, 2.5V, 3.3V & 5V) variants available. It is also requires minimal external circuitry with only a single input and
output capacitor required. 

Where possible the SOT-223 version should be used, but if thermal considerations do not allow this, the next preferred
option is using the TO-252 (also referred to by its branded name DPAK). As a bonus, these two footprints are compatible.
This means that the a SOT-223 part can be mounted onto a TO-252 footprint. Since the SOT-223 part includes a pin 2 while
the TO-252 parts usually do not, it is important to use the TO-252-3_TabPin2 footprint in KiCad. This adds the additional
pad for pin 2 and connects the tab to the same net as pin 2 (Vout).

![An image showing a comparison between the DPAK and SOT-223 footprints.](SOT-223_and_DPAK.JPG "DPAK vs SOT-223") {width="450" thumbnail="true" border-effect="line"}

## CAN Bus

Since the main communication protocol on the car is CAN, any board that needs to communicate with any other parts of the
vehicle also needs to be compatible with the CAN bus protocol. While some microcontrollers (such as the STM32F303) 
has a CAN controller built-in and only require an external transceiver, others require both a CAN controller as well 
as transceiver.

### CAN Transceiver

The MCP2562 and equivalent part MCP2562FD in the SOIC-8 package have been selected as the preferred CAN transceivers to
use on team made PCBs. These transceivers require a 5V supply voltage but also include a Vio pin to interface with a 3.3V
logic level system. Where both the supply voltage and logic level is 5V, the transceiver's Vio pin can simply by tied to
5V. As it is usual for ICs it requires a standard 100nF decoupling capacitor on both the Vdd and Vio pins. 

The MCP2562 series has built in ESD protection up to ±8kV which should be plenty for our purpose. Hence no external ESD
protection is required on the CANH and CANL pins. 

### CAN Controller

The CAN controller used commonly is the MCP2515, although with the shift to using STM32s this will be used less and less
hopefully. 
