# Lab 2: David Pěčonka

### GPIO control registers

1. Complete the table for DDRB and PORTB control register values.

   | **DDRB** | **PORTB** | **Direction** | **Internal pull-up resistor** | **Description** |
   | :-: | :-: | :-: | :-: | :-- |
   | 0 | 0 | input | no | tri-state, high-impedance |
   | 0 | 1 | input | yes | PXN will source current if ext. pulled low |
   | 1 | 0 | output | no | output low |
   | 1 | 1 | output | no | output high |

### GPIO library

2. Complete the table with code sizes from three versions of the blink application.

   | **Version** | **Size [B]** |
   | :-- | :-: |
   | Arduino-style     | 480 |
   | Registers         | 182 |
   | Library functions | 182 |

### Traffic light

3. Scheme of traffic light application with one red/yellow/green light for cars, one red/green light for pedestrians, and one push button. Connect AVR device, LEDs, resistors, push button (for pedestrians), and supply voltage. The image can be drawn on a computer or by hand. Always name all components and their values!

   ![Schematic](https://github.com/xpecon00/digital_electronics_2/blob/main/lab2_gpio_library/test/images/sch%C3%A9ma.jpg)
