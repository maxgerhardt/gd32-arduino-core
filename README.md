# THIS REPO IS NOT DEVELOPED FURTHER
# SEE NEW ARDUINO CORE DEVELOPMENTS AT https://github.com/CommunityGD32Cores/ArduinoCore-GD32

# GD32 Arduino Core

A Arduino core implementation for some GD32 type chips, at first focusing on GD32F1x0 type chips. 

## Movatition

Why create our own Arduino core? 

* Some GD32 chips are drop-in-replacements of STM32 chips, e.g., the STM32F103 and GD32F103
   * the GD32 chips sometimes have extended capabilities though, e.g. running at a higher clock speed due to one bit more in the PLL multiplier registers
   * the standard Arduino STM32 cores such as https://github.com/stm32duino/Arduino_Core_STM32 and https://github.com/rogerclarkmelbourne/Arduino_STM32/ should technically work with it
* Some GD32 chips are not close enough clones / different chips compared to existing STM32 ones
    * e.g., GD32F170, GD32F190, ...
    * for these, no Arduino core exists of yet (that is publically known). Though luck if you wanted to use Arduino with them.
    * => we can fill a gap here for these chips
* Still, using the above Arduino STM32 core with some enabled features is strictly speaking legally forbidden, due to the core using STM32 middleware USB libraries [here](https://github.com/stm32duino/Arduino_Core_STM32/blob/master/License.md#Ultimate-Liberty-License), which has a license stating it *may only run on STM32 parts*. Running it on GD32 chips violates that.
     * (from https://www.st.com/SLA0044) "This software or any part thereof, including modifications and/or derivative works of this software, must be used and execute solely and exclusively on or in combination with a microcontroller or microprocessor device manufactured by or for STMicroelectronics."
   * => We can make a new Arduino core free of these licensing issues by carefully choosing the included (or non-included / self-written) code

## Collaborating

Interested in collaborating? Join our dedicated Discord channel for this at https://discord.gg/59kf4JxsRM.

## State of the project

This project is currently in a planing phase with no code written yet. 

A custom dev board has been designed to make development uniform / reproducable.

## ToDo List (subjecto to change)

* Hardware Design
   * [X] Design custom PCB for development
   * [X] Submit for manufacturing
   * [ ] Get PCBs back
   * [ ] Distribute to devs
   * [ ] Verify and test PCBs (with e.g. simple SPL firmwares)
* Software Design
   * [ ] Decide on questions that influence the core design, e.g.
      * [ ] Depend on / call into SPL framework by GigaDevice, or write own baremetal drivers?
           * flash savings and customizability vs simplicity / development speed
           * also has implications on used licence? 
      * [ ] PlatformIO integration first, Arduino IDE integration later? 
      * [ ] Software USB implementation for chips not supporting USB? 
      * [ ] What exact chips need a custom Arduino core because they are not clones of some STM32 chip (and thus https://github.com/stm32duino/Arduino_Core_STM32 applies) 
      * [ ] etc. etc.
   * [ ] decide on possible project license 
        * different ones for different parts of code (external and internal)?
        * Arduino Core API (https://github.com/arduino/ArduinoCore-API/) is LGPL I think?
## Updates / History

_31.05.2021:_

Initial contact and thoughts about an Arduino core implementation with @kemotz via Email.

_02.06.2021:_

Creation of the Github project and the discord channel.

_10.06.2021:_

A custom dev board has been designed and is in production. The repo with the files for it is at https://github.com/kemotz/GD32F1x0-dev-brd. 

![grafik](https://user-images.githubusercontent.com/26485477/121490451-4eab5380-c9d5-11eb-867f-b4cba305374b.png)
![grafik](https://user-images.githubusercontent.com/26485477/121490465-53700780-c9d5-11eb-8b05-18b1cfc1b38f.png)
![grafik](https://user-images.githubusercontent.com/26485477/121490480-579c2500-c9d5-11eb-8b5b-e1f91f3fcd5e.png)
