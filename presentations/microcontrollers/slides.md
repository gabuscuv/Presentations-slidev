---
theme: ../../theme
title: Getting Started with Slidev Multideck
description: Learn how to use this multi-presentation template
date: 2025-01-01
tags: [tutorial, slidev, template]
listed: true
transition: slide-left
mdc: true
---

<TitleSlide />

---

## Why Microcontrollers?

<Youtube id="fMQwZRW1wng" class="h-full w-full" />

---

### Okay, I didn't understood a shit, Could You explain in human terms

## Introduction to the MicroControllers

- A Microcontroller is a All in one Solution that includes low-power Processor, memory and storage in a small package
- It's thought mainly for repetitive, specific tasks:
  - Example:
    - Microwaves
      - Control the Input, Internal Clock, the Timer.
    - Smart Thermostats
    - Pedemeters
    - Clocks

(Nowadays are quite popular for Internet of things)


---

## What is a Tamagochi?

- It's a gadget launched by 90's by Bandai <img class="inline h-70 absolute right-40" src="./img/gadgets/Tamagotchi.jpg" />
- It's about take care of a alien creature
- It uses RealTime Clock for produce different states 
  - Hungry
  - Happiness
  - Traning
  - Sickness
- Also has a Life Cycle system making age.

---

### Okay Watson, I think everybody knows what's

## What's Actually the Tamagochi Hardware?

- A MicroController <img v-after src="./img/tamagotchi-internals.jpg" class="h-69 inline absolute right-5" />
  - early ones: a Epson MCU E0C6S46/48 [^1][]
  - late ones: SunPlus/GeneralPlus GPLB5X MOS6502 - based [^2][]
- LCD Display
- Three Button Layout
- Speaker
- IR (Since Tamagotchi Collection)


<div class="bottom-5 right-5 w-90 flex absolute text-xs">
<div class="relative top-5">
    <div>[^1] https://github.com/jcrona/tamalib/#hardware-information</div>
    <div>[^2] For more information about these  Natalie Silvanovich "Even More Tamagotchis Were Harmed in the making of the presentation"</div>
</div>
<img v-after src="./img/natalie-talk.png" class="h-30 inline relative " />
</div>
---

## What's the options If I want to make a Tamagochi right now

<!-- Ofc, now days, You can still buy microcontrollers that are way more powerful than the original tamagochis MicroControllers.
You take in mind, The Tamagochi ones are known as Integrated Microcontrollers. (The Microcontroller + thingies)
The choice of the microcontroller determine the limits of the complexity the game.  -->
  <img src="./img/MicroControllers/ESP32-DevKitC-32E_SPL.webp" class="h-30 inline absolute right-3" />

- ESP-32
  - Xtensa CPU (S3 are ideal for 2D Image Tansform and Video Playback... poorly)
  - RISC-V CPU (Quite cheap)
- NXP (Power, ARM)   <img src="./img/MicroControllers/NXP_CHIP.jpg" class="h-30 inline absolute right-3" />
- STM32 (ARM Cores)
- Raspberry Pi Pico
- Arduino

---

## What's the options If I want to make a Tamagochi right now

### Oldschool MicroControllers: 
<img src="./img/gadgets/stuff.webp" class="h-40 inline" />
<img src="./img/gadgets/Symthphonic.png" class="h-40 inline" />
<img src="./img/gadgets/displayattached.webp" class="h-40 inline" />


### Integrated MicroControllers Manufacturer:
<img src="./img/IntegratedMicroControllers/M5Stack-PAPER.webp" class="h-80 inline top-60 absolute right-3" />
<img src="./img/IntegratedMicroControllers/1.85inch-touch-lcd-module-3.jpg" class="h-30 inline absolute bottom-43 left-130" />
<img src="./img/IntegratedMicroControllers/T-Embed-K167-LILYGO_11.webp" class="h-40 bottom-4 inline absolute left-60" />
<img src="./img/IntegratedMicroControllers/T-DECK-PLUS_6.jpg" class="h-40 bottom-4 inline absolute right-90" />

- Waveshare
- LILYGO
- M5 Stack
- Adafruit

---

## Language Supported:

### Programming Language Supported

<div class="flex">
  <img class="h-20 w-20" src="./img/programminglanguage/C_Programming_Language.svg" />
  <img class="h-20 w-70 ml-5" src="./img/programminglanguage/micropython-logo.png" />
</div>

### Graphics Library Standards

<div class="flex">
  <img class="w-140 h-20" src="./img/misc/rawdata.png" />
  <img class="w-35" src="./img/frameworks/lvgl-logo.png" />
  <img class="w-20 h-20" src="./img/frameworks/Raylib_logo.png" />
</div>

---

### cool, What kind of games can I make with these thingies

## Game Design applied to MicroControllers (1)

- Standalone
  - Tamagochi
  - Nintendo Game & Watch (Sharp SM510, NEC uCom-43)
  <div class="top-35 ml-10 absolute left-50 flex inline ">
  <img class="h-15" src="./img/gadgets/Game-and-watch-ball.png" />
    <img class="h-15 ml-10" src="./img/gadgets/Tamagotchi.jpg" />
  </div>  

  <img class="h-45 inline absolute top-30 right-4"   src="./img/gadgets/vmu-dreamcast.png" />
  <img class="h-60 absolute right-4 bottom-0 inline"  src="./img/gadgets/gba-gcn.webp" />
 <!-- https://www.youtube.com/watch?v=Rwp9Mqwu8zs -->
  
  <img class="h-30 absolute bottom-30 right-50 inline" src="./img/gadgets/PSP-PS3.jpg" />
  <img class="h-30 absolute bottom-2 left-90 inline" src="./img/Controller/DK-Bongos.jpg" />

- Companion Device
  - GBA (with GameCube Mode) - Dumb Terminals 
  - PSP (With PS3) - Resistance Retribution
  - VMU (Dreamcast)
  - PokeWalker
- Accessories
  - Rythm Accesories


---

### BadassGotchi

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

### Castanets ESP32

## Use Case 2a (Accessories)

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

## Use Case 2b (Accessories)

### Mercacompra 2030

https://geri8.itch.io/mercacompra2030

---

## Use Case 3a (Companion Devices)

### Treasure-Search/Radar Cooperative Game

<div class="w-100 h-50 flex">
  <img src="./img/MicroControllers/EspressIf-ESP32-S3-DevKitC-N8R8.jpg" class="" />
  <img src="./img/IntegratedMicroControllers/1.85inch-touch-lcd-module-3.jpg"  />
  <img src="./img/frameworks/Raylib_logo.png" />
</div>


---

## Use Case 3b (Companion Devices)

### Cooperative Game

<div class="w-100 h-50 flex">
  <img src="./img/MicroControllers/EspressIf-ESP32-S3-DevKitC-N8R8.jpg" class="" />
  <img src="./img/IntegratedMicroControllers/1.85inch-touch-lcd-module-3.jpg"  />
  <img src="./img/frameworks/Raylib_logo.png" />
  <img class="p-1" src="./img/games/KeepTalkingNoBodyExplodes.jpg" />
</div>

---

## Can I Use A Microcontroller as a Tamagotchi...

### Of course

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

# One more thing

## Proxima Meetup

- [Jose Escribano](https://www.mobygames.com/person/567289/jose-antonio-escribano-ayllon/) Vuelve
- [Rubus / @KaruArts](https://www.artstation.com/karuarts) Saca nuevo Juego 
  - Charla: "Porqué siempre debes hacer caso a esa vocecilla de tu cabeza y comprobar que el trademark esté libre en vez de fiarte del resto del equipo para evitar problemas legales que te impidan sacar el puto que lleva hecho un par de meses porque un cryptobro mamahuevos te da problemas"
- [Una Posibilidad](https://www.mobygames.com/person/909352/alejo-silos-leal/)
