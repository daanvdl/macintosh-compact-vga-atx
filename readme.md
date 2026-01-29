# Macintosh 128K / 512K / Plus VGA (ATX Powered) Board

Compact test & bench board to run a Macintosh 128K / 512K / 512Ke / Plus logic board outside the case, powered by a standard ATX power supply, with VGA video output.

Ideal for troubleshooting, repair, and video capture.

---

## Firmware

Prebuilt Pico firmware is included:

* **Pico 1**: `firmware/pico1.uf2`
* **Pico 2**: `firmware/pico2.uf2`

Flash the UF2 file to the Pico using standard USB boot mode.

### Signal timing note

When using different brands or batches of level shifters, small variations in signal propagation delay can occur.  
These timing differences may affect VGA signal stability or image clarity.

If you experience unstable sync, noise, or an unclear image, try the alternative timing variants to achieve the best and most stable VGA output for your specific hardware configuration. Alternative firmware builds with slightly adjusted video timing are provided in:
* `firmware/timing_alternatives/`

---

## PCB / Gerbers

Gerber files:

```
gerber/plus_vga.zip
```

---

## Components

* Raspberry Pi **Pico 1 or Pico 2**
* Angled VGA connector
* 4-channel level shifter
* 24P ATX straight connector
* 1x Male 11P CH3.96 straight connector
* 2× 660 Ω resistors
* 1× 100 Ω resistor
* 2× 2.54mm pinheader
* 2.54mm jumper for power-on

---

## Firmware source & credits

The Pico firmware included in this repository is compiled from the open-source project:

**mac-se-video-converter**  
https://github.com/guruthree/mac-se-video-converter

This project provides the Raspberry Pi Pico–based Macintosh video capture and VGA output implementation used on this board.

The UF2 files in the `firmware/` directory were compiled from this codebase, with timing parameters and configuration selected to work reliably with Macintosh 128K / 512K / 512Ke / Plus logic boards.

All credit for the original firmware and video conversion logic goes to the original author(s) of the `mac-se-video-converter` project.

Please refer to the original repository for source code, license information, and further documentation.
