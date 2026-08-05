# Cheapino v2: Personal Build Notes

## Case Modifications

This is a **v2 build**. I slightly modified the original case to better suit my preferences — adjusted some tolerances to fit hardware I sourced locally (India) and simplified the geometry for support-free printing.

| Feature | Modification Details |
| :--- | :--- |
| M2 Insert Holes | Diameter changed to `3.65 mm` to perfectly fit standard M2 brass inserts. |
| Rubber-Foot Pockets | Resized for 8×2 mm (or 8×3 mm) silicone bumpers. |
| Countersinks | Added a 3-tier countersink to ensure M2 CSK screws seat perfectly flush. |
| Switch Clips | Reduced cutout thickness to `1.45 mm` for a tighter, more secure grip on the switches. |
| Case Chamfer | Reduced the outer edge chamfer (personal preference). |
| RJ45 Cutout | Simplified the overhang geometry to allow completely support-free printing. |

## 3D Printing

**Bambu Studio project:** [`case/print-profiles/cheapino-case-bambu.3mf`](../case/print-profiles/cheapino-case-bambu.3mf)

I have included a pre-configured print profile for Bambu Lab printers. The `.3mf` file contains the full 4-part plate arranged so **no supports are needed**.

It also includes two variants of a custom flush-fit encoder knob (D-shaft and round/knurled for a 15 mm shaft) designed to sit close to the top of the case. Print the knob that matches your specific EC11 encoder.

If the fit needs adjusting, you can grab the source `.step` or `.f3d` files for the knob from [Printables](https://www.printables.com/model/1794223).


## PCB Fabrication

For how to order (uploading gerbers, settings, etc.), see the [ordering guide](orderingguide.md#the-pcb).

For India, use [Robu.in](https://robu.in/pcb-manufacturing/) or [Zbotic.in](https://zbotic.in/pcb-manufacturing/), which proxy your order to JLCPCB while handling shipping and customs. Ordering from JLCPCB directly might be cheaper but customs clearance in India is unpredictable, so probably not worth the risk.

## Bill of Materials

### Electronics

| Part | Qty | Description/Notes | Sourcing Links |
| :--- | ---: | :--- | :--- |
| Waveshare RP2040-Zero | 1 | **Must NOT** have pre-soldered headers. | [Robu (Original)](https://robu.in/product/waveshare-rp2040-zero-without-header/), [Robu (Clone)](https://robu.in/product/rp2040-zero-for-raspberry-pi-microcontroller-with-soldering/) |
| Male Pin Headers | 1 | 2.54 mm 1×40 straight strip. | [Robu](https://robu.in/product/2-54mm-1x40-pin-male-single-row-straight-short-header-strip-pack-of-3/) |
| 1N4148 Diodes | 42 | Through-hole. One per key + a few spares. | [Vishaworld](https://vishaworld.com/products/1n4148-diode), [Robu](https://robu.in/product/1n4148-1w-zener-diode-pack-of-50) |
| EC11 Rotary Encoder | 1 | 15 mm shaft. Match your 3D printed knob to the shaft type. | [Robu (D-shaft)](https://robu.in/product/hongyan-ec11h-7ce15p1zd15f7-rotary-encoder-with-push-button-switch-vertical-plug-in-5-pin-360-degree/), [Robu (Round)](https://robu.in/product/hongyan-ec11h-7ce15p1zy15f7-rotary-encoder-with-push-button-switch-vertical-plug-in/) |

### Hardware (Case Assembly)

| Part | Qty | Description/Notes | Sourcing Links |
| :--- | ---: | :--- | :--- |
| M2 Brass Heatset Inserts | 18 | M2 × 4 mm, OD 3.8 mm (Tested in this build). | [OnlyScrews](https://onlyscrews.in/products/m2-x-4mm-brass-threaded-inserts) |
| M2 Brass Heatset Inserts | 18 | M2 × 3 mm, OD 3.8 mm (Alternative, untested). | [OnlyScrews](https://onlyscrews.in/products/m2-x-3mm-brass-threaded-inserts) |
| M2 Countersunk Screws | 18 | M2 × 6 mm, Phillips flat head (Sits flush with case). | [OnlyScrews](https://onlyscrews.in/products/m2-x-6mm-phillips-csk-ss-304-screw-dia-2mm-length-6mm) |
| Silicone Rubber Feet | 8 | 8×2 mm (or 8×3 mm) tall. | [Amazon](https://www.amazon.in/gp/product/B083DTH5HL) |
| Flush-fit Knob | 1 | 3D printed part. | [Printables](https://www.printables.com/model/1794223) |


## Related Docs

* [Ordering guide](orderingguide.md) — Full electronics BOM with AliExpress links.
* [Case build guide](case_buildguide.md) — Assembly instructions, heat-set install, and screw torque.
* [Build guide v2](buildguide_v2.md) — Soldering and PCB assembly.
