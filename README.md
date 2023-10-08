# sfp-snoop

SFP(+) cape for the [VCC-GND](https://vcc-gnd.com) [YD-RP2040](http://152.32.187.208:8080/yd-data/YD-RP2040/) pending a few modifications.

![sfp-snoop-pcbdraw-front](https://github.com/up-n-atom/sfp-snoop/assets/234549/daa11510-efba-476f-8820-78944d1af42e) ![sfp-snoop-pcbdraw-back](https://github.com/up-n-atom/sfp-snoop/assets/234549/498c303e-8316-4b18-bb49-32507602fd6e)

## Necessary YD-RP2040 Modifications

1. __Remove__ *D2, F1, U1, C1, C2*
2. __Bridge__ *D2* pins 1 and 2 with a 0Ohm 0603 resistor

__U1__ *(ME6215C33M5G)* and supporting components on the YD-RP2040 are replaced by __U1__ *(AIC1221-33GY3TR)* on the sfp-snoop 

![YD-RP2040-RP2040-vcc-gnd-studio-Micropython-CircuitPython-Arduino-Raspberry-Pi-Pico-PLUS-MCU-Board-microcontroller](https://github.com/up-n-atom/sfp-snoop/assets/234549/8e12fa5b-a43b-4a43-b1c5-90607dd3d33b)

## Pinout

| YD-RP2040 | [SFP (INF-8074i)](https://members.snia.org/document/dl/26184) | Transceivers |
| --        | --              | -- |
| 7 (GP5 - *USART1 RX*)   | 2 | Huawei SmartAX MA5671A, Alcatel-Lucent G-010S-P, BFW WAS-110 UART TX |
| 12 (GP8 - *USART1 TX*)  | 3 | Nokia G-010S-A UART RX |
| 9 (GP6 - *I2C1 SDA*)    | 4 | |
| 10 (GP7 - *I2C1 SCL*)   | 5 | |
| 11 (GP9 - *USART1 RX*)  | 6 | Nokia G-010S-A UART TX |
| 6 (GP4 - *USART1 TX*)   | 7 | Huawei SmartAX MA5671A, Alcatel-Lucent G-010S-P, BFW WAS-110 UART RX |
| 5 (GP3)                 | 8 | |
| 29 (GP22)               | 9 | |

* Short JP1
* Short R10 jumper to pin 37 (GP23) for user button power switch, or populate R10 with a 10KOhm 0603 resistor to access RGB LED (GP23)

## Bill of Materials

Total cost for single unit, incl. YD-RP2040 is around $5 USD.

| Ref.            | Value  | [LCSC](https://www.lcsc.com/) | Qty. |
| --              | --     | --                            | --:  |
| C1, C2          | 4.7uF  | [C1872](https://www.lcsc.com/product-detail/Multilayer-Ceramic-Capacitors-MLCC-SMD-SMT_Samsung-Electro-Mechanics-CL31B475KAHNNNE_C1872.html) | 2    |
| C3, C6, C9, C11 | 0.1uF  | [C282519](https://www.lcsc.com/product-detail/Multilayer-Ceramic-Capacitors-MLCC-SMD-SMT_CCTC-TCC0603X7R104K500CT_C282519.html) | 4    |
| C4              | 150uF   | [C542620](https://www.lcsc.com/product-detail/Tantalum-Capacitors_PANASONIC-6TPE150MAPB_C542620.html) | 1    |
| C5, C8          | 1uF    | [C59302](https://www.lcsc.com/product-detail/Multilayer-Ceramic-Capacitors-MLCC-SMD-SMT_FH-Guangdong-Fenghua-Advanced-Tech-0603B105K250NT_C59302.html) | 2    |
| C7, C10         | 0.01uF | [C525264](https://www.lcsc.com/product-detail/Multilayer-Ceramic-Capacitors-MLCC-SMD-SMT_PSA-Prosperity-Dielectrics-FN18X103K500PSG_C525264.html) | 2    |
| F1              | 2A     | [C261954](https://www.lcsc.com/product-detail/Resettable-Fuses_TLC-Electronic-TLC-NSMD100_C261954.html) | 1    |
| J1              | SFP+   | [C210158](https://www.lcsc.com/product-detail/Card-Edge-Connectors_TE-Connectivity-1367073-1_C210158.html) | 1    |
| J1 (Optional)   | SFP+ Cage   | [C7429382](https://www.lcsc.com/product-detail/Connector-Shells_HCTL-HC-SFP-03L_C7429382.html) | 1    |
| R1-R10           | 10KOhm | [C25804](https://www.lcsc.com/product-detail/Chip-Resistor-Surface-Mount_UNI-ROYAL-Uniroyal-Elec-0603WAF1002T5E_C25804.html) | 9 |
| U1              | AIC1221-33GY3TR | [C211622](https://www.lcsc.com/product-detail/Linear-Voltage-Regulators-LDO_AIC-Analog-Integrations-AIC1221-33GY3TR_C211622.html) | 1 |
| U2              | AP2191WG-7 | [C141321](https://www.lcsc.com/product-detail/Power-Distribution-Switches_Diodes-Incorporated-AP2191WG-7_C141321.html) | 1 |


| Ref.             | Value  | [AliExpress](https://www.aliexpress.com/) | Qty. |
| --               | --     | --                                        | --:  |
| P1, P2 *YD-RP2040* | Male   | [21mm height, 2.54mm pitch, 40-pin Male Header](https://www.aliexpress.com/item/1005001809920855.html) | 1 |
| J2, J3 *sfp-snoop* | Female | [2.54mm pitch, 20-pin Female Header](https://www.aliexpress.com/item/4000386969080.html) | 1 |
