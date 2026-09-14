---
theme: ../../theme
title: "Tamagotchis, Companion Devices & Castanets"
description: "Introduction to MicroControllers"
date: 2026-09-14
listed: true
transition: slide-left
mdc: true
---

<TitleSlide />

---

## <THeader k='microcontrollers.why' />

<Youtube v-click id="fMQwZRW1wng" class="h-full w-full" />

---

### <THeader k='microcontrollers.explanationQuestion' />

## <THeader k='microcontrollers.introduction' />

- <T k='microcontrollers.definition' />
- <T k='microcontrollers.specificTasks' />
  - <T k='microcontrollers.examples' />
    - <T k='microcontrollers.microwaves' />
      - <T k='microcontrollers.microwaveControls' />
    - <T k='microcontrollers.smartThermostats' />
    - <T k='microcontrollers.pedemeters' />
    - <T k='microcontrollers.clocks' />
<T k='microcontrollers.iot' />

---

## <THeader k='tamagotchi.whatIs' />

- <T k='tamagotchi.bandai' /> <img class="inline h-70 absolute right-30" src="./img/gadgets/Tamagotchi.jpg" />
- <T k='tamagotchi.care' />
- <T k='tamagotchi.realTimeClock' />
  - <T k='tamagotchi.hungry' />
  - <T k='tamagotchi.happiness' />
  - <T k='tamagotchi.training' />
  - <T k='tamagotchi.sickness' />
- <T k='tamagotchi.lifeCycle' />

---

### <THeader k='tamagotchi.hardwareJoke' />

## <THeader k='tamagotchi.hardwareTitle' />

- <T k='tamagotchi.microcontroller' /> <img v-after src="./img/tamagotchi-internals.jpg" class="h-69 inline absolute right-5" />
  - <T k='tamagotchi.earlyModels' /><div v-after>Epson MCU E0C6S46/48 [^1][]</div>
  - <T k='tamagotchi.lateModels' /><div v-after> SunPlus/GeneralPlus GPLB5X MOS6502 - based [^2][]</div>
- <T k='tamagotchi.lcd' />
- <T k='tamagotchi.buttons' />
- <T k='tamagotchi.speaker' />
- <T k='tamagotchi.ir' />

<div class="bottom-5 right-5 w-90 flex absolute text-xs">
<div class="relative top-5">
    <div>[^1] https://github.com/jcrona/tamalib/#hardware-information</div>
    <div>[^2] For more information about these  Natalie Silvanovich "Even More Tamagotchis Were Harmed in the making of the presentation"</div>
</div>
<img v-after src="./img/natalie-talk.png" class="h-30 inline relative " />
</div>
---

## <THeader k='microcontrollers.currentOptions' />

<!-- Ofc, now days, You can still buy microcontrollers that are way more powerful than the original tamagochis MicroControllers.
You take in mind, The Tamagochi ones are known as Integrated Microcontrollers. (The Microcontroller + thingies)
The choice of the microcontroller determine the limits of the complexity the game.  -->
  <img src="./img/MicroControllers/ESP32-DevKitC-32E_SPL.webp" class="h-30 inline absolute right-3" />

- ESP-32
  - Xtensa CPU (S3 are ideal for 2D Image Tansform and Video Playback... poorly)
  - RISC-V CPU (Quite cheap)
- NXP (Power, ARM) <img src="./img/MicroControllers/NXP_CHIP.jpg" class="h-30 inline absolute right-3" />
- STM32 (ARM Cores)
- Raspberry Pi Pico
- Arduino

---

## <THeader k='microcontrollers.currentOptions' />

<div v-click>

### <THeader k='microcontrollers.oldschool' />

<img src="./img/gadgets/stuff.webp" class="h-40 inline" />
<img src="./img/gadgets/Symthphonic.png" class="h-40 inline" />
<img src="./img/gadgets/displayattached.webp" class="h-40 inline" />

</div>

<div v-click>

### <THeader k='microcontrollers.integrated' />

<img src="./img/IntegratedMicroControllers/M5Stack-PAPER.webp" class="h-80 inline top-60 absolute right-3" />
<img src="./img/IntegratedMicroControllers/1.85inch-touch-lcd-module-3.jpg" class="h-30 inline absolute bottom-43 left-130" />
<img src="./img/IntegratedMicroControllers/T-Embed-K167-LILYGO_11.webp" class="h-40 bottom-4 inline absolute left-60" />
<img src="./img/IntegratedMicroControllers/T-DECK-PLUS_6.jpg" class="h-40 bottom-4 inline absolute right-90" />

- Waveshare
- LILYGO
- M5 Stack
- Adafruit

</div>

---

## <THeader k='languages.supported' />

### <THeader k='languages.programming' />

<div class="flex">
  <img v-click class="h-20 w-20" src="./img/programminglanguage/C_Programming_Language.svg" />
  <img v-click class="h-20 w-70 ml-5" src="./img/programminglanguage/micropython-logo.png" />
</div>

### <THeader k='languages.graphicsLibraries' />

<div class="flex">
  <img v-click class="w-140 h-20" src="./img/misc/rawdata.png" />
  <img v-click class="w-35" src="./img/frameworks/lvgl-logo.png" />
  <img v-click class="w-20 h-20" src="./img/frameworks/Raylib_logo.png" />

</div>

---

### <THeader k='gameDesign.whatCanIDo' />

## <THeader k='gameDesign.microcontroller' />

- <T k='gameDesign.standalone' />
<div v-after>
  
  - Tamagotchi
  - Nintendo Game & Watch (Sharp SM510, NEC uCom-43)
  <div  class="top-35 ml-10 absolute left-50 flex inline ">
  <img class="h-15" src="./img/gadgets/Game-and-watch-ball.png" />
    <img class="h-15 ml-10" src="./img/gadgets/Tamagotchi.jpg" />

  </div>
</div>
<div v-click>
  <img class="h-45 inline absolute top-30 right-4" src="./img/gadgets/vmu-dreamcast.png" />

  <img class="h-60 absolute right-4 bottom-0 inline" src="./img/gadgets/gba-gcn.webp" />

  <img class="h-30 absolute bottom-30 right-50 inline" src="./img/gadgets/PSP-PS3.jpg" />



- <T k='gameDesign.companionDevice' />

  - GBA (with GameCube Mode) - Dumb Terminals
  - PSP (With PS3) - Resistance Retribution
  - VMU (Dreamcast)
  - PokeWalker

</div>
  
- <T k='gameDesign.accessories' />

  - <T k='gameDesign.rhythmAccessories' />
  - <img v-after class="h-30 absolute bottom-2 left-90 inline" src="./img/Controller/DK-Bongos.jpg" />

---

### **CutreGotchi**

## <THeader k='useCases.accessories1' />


- LVGL
- Waveshare ESP32-S3-Touch-LCD-1.85
- Display: 360 × 360 pixels (262K colors)
  - Touch Panel: Capacitive touch controlled via I2C
  - QMI8658 6-axis gyroscope and accelerometer
  - Onboard audio decoding chip with built-in microphone and speaker support

<div class="w-100 h-50 flex">
  <img src="./img/IntegratedMicroControllers/1.85inch-touch-lcd-module-3.jpg"  />
  <img src="./img/frameworks/lvgl-logo.png" />
</div>
---

### **Castanets ESP32**

## <THeader k='useCases.accessories2a' />

- A Controller <img src="./img/MicroControllers/EspressIf-ESP32-S3-DevKitC-N8R8.jpg" class="inline absolute left-110 h-30" />
  - EspressIf ESP32-S3 (Xtensa) N8R8
  - Connectability: ESP-NOW, USB-Serial

<div class="inline left-100 absolute flex">
  <img src="./img/MicroControllers/seeed-studio-xiao-esp32-c3.png" class="h-20" />
  <img src="./img/MicroControllers/seeed-studio-xiao-esp32-c6.jpg" class="h-22" />
</div>

- Satellites 
  - ESP32-C3 & ESP32-C6 (RISC-V) 
  - Connectability: ESP-NOW
  - GPIO <img src="./img/Controller/Piezo_LM797.jpg" class="inline h-50" />
    - (for Piezo)


  
<div class="absolute top-30 right-10">

```mermaid
flowchart TD
    A[Satellite] -->|ESP Now| Endpoint
    B[Satellite] -->|ESP Now| Endpoint
    C[Bluetooth HID] -->|Bluetooth| Endpoint
    Endpoint[Controller] -->|USB Serial| Computer[Computer]
```

</div>

---

## <THeader k='useCases.accessories2b' />

### **Mercacompra 2030**

https://geri8.itch.io/mercacompra2030

---

## <THeader k='useCases.companion3a' />

### <THeader k='useCases.treasureRadar' />

<div class="w-100 h-50 flex">
  <img src="./img/MicroControllers/EspressIf-ESP32-S3-DevKitC-N8R8.jpg" class="" />
  <img src="./img/IntegratedMicroControllers/1.85inch-touch-lcd-module-3.jpg" />
  <img src="./img/frameworks/Raylib_logo.png" />
</div>

---

## <THeader k='useCases.companion3b' />

### <THeader k='useCases.cooperativeGame' />

<div class="w-100 h-50 flex">
  <img src="./img/MicroControllers/EspressIf-ESP32-S3-DevKitC-N8R8.jpg" class="" />
  <img src="./img/IntegratedMicroControllers/1.85inch-touch-lcd-module-3.jpg" />
  <img src="./img/frameworks/Raylib_logo.png" />
  <img class="p-1" src="./img/games/KeepTalkingNoBodyExplodes.jpg" />
</div>

---

## <THeader k='tamagotchi.canUseMicrocontroller' />

### <THeader k='tamagotchi.ofCourse' />

<img class="h-100 items-center" src="./img/misc/Tamagotchi.png" />

---
src: ../../slides/closing/questions.md
---

---
src: ../../slides/closing/thank-you.md
---

---
layout: image
background: ./img/CGD_bg.jpg
image: ./img/CGD_bg.jpg
---

# <T k='closing.oneMoreThing' />

## Proxima Meetup

<div v-click>

- [Jose Escribano](https://www.mobygames.com/person/567289/jose-antonio-escribano-ayllon/) Vuelve

</div>

<div v-click>

- [Rubus / @KaruArts](https://www.artstation.com/karuarts) Saca nuevo Juego 
  - Charla: "Porqué siempre debes hacer caso a esa vocecilla de tu cabeza y comprobar que el trademark esté libre en vez de fiarte del resto del equipo para evitar problemas legales que te impidan sacar el puto que lleva hecho un par de meses porque un cryptobro mamahuevos te da problemas"

</div>

<div v-click>

- [Una Posibilidad](https://www.mobygames.com/person/909352/alejo-silos-leal/)

</div>