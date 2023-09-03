# sfp-snoop

SFP(+) cape for the [VCC-GND](https://vcc-gnd.com) [YD-RP2040](http://152.32.187.208:8080/yd-data/YD-RP2040/) pending a few modifications.

![sfp-snoop-pcbdraw-front](https://github.com/up-n-atom/sfp-snoop/assets/234549/daa11510-efba-476f-8820-78944d1af42e) ![sfp-snoop-pcbdraw-back](https://github.com/up-n-atom/sfp-snoop/assets/234549/d36995ab-db5e-42ed-af4a-bb10313b0962)

## Necessary YD-RP2040 Modifications

1. __Remove__ *D2, F1, U1, C1, C2*
2. __Bridge__ *D2* pins 1 and 2 with a 0Ohm 0603 resistor

__U1__ *(ME6215C33M5G)* and supporting components on the YD-RP2040 are replaced by __U1__ *(AIC1221-33GY3TR)* on the sfp-snoop 

![YD-RP2040-RP2040-vcc-gnd-studio-Micropython-CircuitPython-Arduino-Raspberry-Pi-Pico-PLUS-MCU-Board-microcontroller](https://github.com/up-n-atom/sfp-snoop/assets/234549/8e12fa5b-a43b-4a43-b1c5-90607dd3d33b)
