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

## What is a Tamagochi?

- It's a virtual pet launched by 90's

---

### Okay Watson, I think everybody knows what's

## What's Actually the Tamagochi Hardware?

- A MicroController <img v-after src="./img/tamagotchi-internals.jpg" class="h-69 inline absolute right-5" />
  - early ones: a Epson MCU E0C6S46
  - late ones: SunPlus/GeneralPlus GPLB5X MOS6502 - based [^1][]
- LCD Display
- Three Button Layout
- Speaker
- IR (Since Tamagotchi Collection)


<div class="bottom-5 right-5 w-90 flex absolute text-xs">
<div class="relative top-12">
    [^1] For more information about these  Natalie Silvanovich "Even More Tamagotchis Were Harmed in the making of the presentation"
</div>
<img v-after src="./img/natalie-talk.png" class="h-30 inline relative " />
</div>
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

### Integrated MicroControllers Manufacturer:
<img src="./img/IntegratedMicroControllers/M5Stack-PAPER.webp" class="h-80 inline top-20 absolute right-3" />
<img src="./img/IntegratedMicroControllers/1.85inch-touch-lcd-module-3.jpg" class="h-30 inline absolute top-43 left-140" />
<img src="./img/IntegratedMicroControllers/T-Embed-K167-LILYGO_11.webp" class="h-40 top-50 inline absolute left-100" />
<img src="./img/IntegratedMicroControllers/T-DECK-PLUS_6.jpg" class="h-50 top-90 inline absolute right-90" />

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
  
  <img class="h-20 absolute top-40 right-35 inline" src="./img/gadgets/Game-and-watch-ball.png" />
  <img class="h-60 absolute right-20 inline" src="./img/gadgets/so-what-exactly-is-the-tingle-tuner-for-v0-555lc7q5cgue1.webp" />
- Companion Device
  - GBA (with GameCube Mode) - Dumb Terminals
    - Windwaker 
  - VMU (Dreamcast)
  - PokeWalker
- Accessories
  - PSP (connected with PS3)
  - Guitar Hero Controller

---

###

## Game Design applied to MicroControllers (2)

---

### How can I connect all this shit

## Networking

```mermaid
flowchart TD
    A[ESP32A] -->|ESP Now| Endpoint
    B[ESP32B] -->|ESP Now| Endpoint
    C[Bluetooth HID] -->|Bluetooth| Endpoint
    Endpoint[Controller] -->|USB Serial| Computer[Computer]
```

---
