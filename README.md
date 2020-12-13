# stm32wl-module-1
A LoRa+MCU module that can be implemented as a tiny PCB (roughly 12 x 11 mm).  It uses the STM32WLE5 IC.  An Arduino-form-factor dev board design is also provided.

## HW Features ##

### Overview ### 
* STM32WLE5 MCU + LoRa Transceiver
* Split TX/RX for maximum sensitivity
* Supports full TX dynamic range via individual high-power and low-power TX paths
* 32.768 kHz high-precision RTC crystal
* 32.000 MHz +/- 1ppm TCXO
* Configurable to use multiple DC supply options:
  * 1.8V + 3.3V (best performance)
  * 1.8V only (low power TX only)
  * 3.3V only
  * 3.3V with user-supplied, off-module LC tank circuit to support integrated DC-DC buck.
  
### PCB specs ###
This is a moderate-density PCB design utilizing a BGA, so it cannot be produced on a low-cost PCB process.  On the plus side, it's so small that the price-per-board is low.
* The module is designed to be produced on the PCBWay 4-layer Stackup at 0.4 mm board thickness, using normal FR-4.  
* It requires blind vias and via-in-pad, although there are __no buried vias__.
* Space / Trace tolerance is 0.075 mm.
* For low-volume garage manufacturing, a 5 x 4 PCB panel works nicely.

### Compatibility with Murata ABZ-type modules ###
This module fits the same footprint as the Murata ABZ-type modules, although it is not pin-compatible.  The pin positions have been kept as close as possible to the corresponding positions on the ABZ modules, but due to the different features of the underlying hardware, some pins have been optimized to different locations.

## CAD Format ##
The project was created in DipTrace.  It's a high quality PCB CAD program at a reasonable price.  Conversions to other CAD file formats are welcome and appreciated, although, at this time, DipTrace is selected as the CAD program for mainline, forward development.

## Licensing ##
The license is GPL v3, which means that derivative works based on this work must be distributed also via GPL v3 or a compatible license.  If you wish to use this work outside the limitations of the GPL v3, please contact the creator (JP Norair) and we can arrange something.  As a personal note, I (JP Norair, creator of LPGSM) am less interested in profiting with money on this particular project than I am with cultivating it into the ultimate reference design for low power RF.  So various forms of in-kind contributions are preferred.

