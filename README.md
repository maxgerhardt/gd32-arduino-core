# GD32 Arduino Core

A Arduino core implementation for some GD32 type chips, at first focusing on GD32F1x0 type chips. 

## Collaborating

Interested in collaborating? Join our dedicated Discord channel for this at https://discord.gg/59kf4JxsRM.

## State of the project

This project is currently in a planing phase with no code written yet. 

A custom dev board has been designed to make development uniform / reproducable.

## ToDo List (subjecto to change)

* Hardware Design
   * [ ] Design custom PCB for development
   * [ ] Submit for manufacturing
   * [ ] Get PCBs back
   * [ ] Distribute to devs
   * [ ] Verify and test PCBs (with e.g. simple SPL firmwares)
* Software Design
   * [ ] Decide on questions that influence the core design, e.g.
      * [ ] Depend on / call into SPL framework by GigaDevice, or write own baremetal drivers?
      * [ ] PlatformIO integration first, Arduino IDE integration later? 
      * [ ] Software USB implementation for chips not supporting USB? 
      * [ ] What exact chips need a custom Arduino core because they are not clones of some STM32 chip (and thus https://github.com/stm32duino/Arduino_Core_STM32 applies) 
      * [ ] etc. etc.

## Updates / History

_31.05.2021:_

Initial contact and thoughts about an Arduino core implementation with @kemotz via Email.

_10.06.2021:_

A custom dev board has been designed and is in production. The repo with the files for it are at https://github.com/kemotz/GD32F1x0-dev-brd. 

![grafik](https://user-images.githubusercontent.com/26485477/121490451-4eab5380-c9d5-11eb-867f-b4cba305374b.png)
![grafik](https://user-images.githubusercontent.com/26485477/121490465-53700780-c9d5-11eb-8b05-18b1cfc1b38f.png)
![grafik](https://user-images.githubusercontent.com/26485477/121490480-579c2500-c9d5-11eb-8b5b-e1f91f3fcd5e.png)
