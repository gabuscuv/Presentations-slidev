---
theme: ../../theme
title: Game Audio Design Using Middlewares
description: Game Audio Design for Videogames Using Middlewares
date: 2025-07-06
listed: true
transition: slide-left
mdc: true
---

<TitleSlide />

---

## <THeader k="slides.what_isnt_this_talk.heading" />

  1. <T k="slides.what_isnt_this_talk.integrated.heading" />
     1. <T k="slides.what_isnt_this_talk.integrated.options" />
<div class="flex ml-50">
<div>
   <T k="slides.what_isnt_this_talk.audioframeworks.heading" />
   
      1. Mozilla CubeB
      2. libsoundio
      3. SDL
      4. OpenAL
      5. FAudio
 </div>
<div>
  <T k="slides.what_isnt_this_talk.ownBackend.heading" />
      
        - WinMM
        - WASAPI
        - PulseAudio / PipeWire
        - Core Audio
        - AudioUnit
        - AAudio
   </div>
</div>

---

## <THeader k="slides.resources.heading" />

1. <T k="slides.resources.items" />  

---

## <THeader k="slides.popular_middlewares.heading" />

<div class="grid grid-cols-2 gap-8">

<div>
<img src="./img/Wwise.png" class="h-24 mx-auto">
<ul>
<li><T k="slides.popular_middlewares.wwise.free" /></li>
<li><T k="slides.popular_middlewares.wwise.paid" /></li>
</ul>
</div>

<div>
<img src="./img/fmod.png" class="h-16 mx-auto">
<ul>
<li><T k="slides.popular_middlewares.fmod.free" /></li>
<li><T k="slides.popular_middlewares.fmod.paid" /></li>
</ul>
</div>

</div>

---

## <THeader k="slides.experience.heading" />

![](./img/GamesWithAudioMiddle.png)

---

## <THeader k="slides.operation_modes.heading" />

1. **<T k="slides.operation_modes.items.0" />**
   - <T k="slides.operation_modes.items.1" />  
     - [<T k="slides.videos.online" />](https://www.youtube.com/watch?v=L6tU6rDpSUA)  
     - [<T k="slides.videos.local" />](./Audio/FMODExample-DynamicMusicwithSFXSounds.mkv)
   - <T k="slides.operation_modes.items.2" />  
     - <T k="slides.operation_modes.items.3" />
2. **<T k="slides.operation_modes.items.4" />**
   - <T k="slides.operation_modes.items.5" />
3. **<T k="slides.operation_modes.items.6" />**
   

<T k="slides.videos.note" />

---
layout: image-right
image: ./img/FMOD_UnrealIntegration_StringTables.png
---

# <THeader k="slides.stringtable.heading" />

- <T k="slides.stringtable.bullets" />

<img src="./img/FMOD_StringTable.png" class="h-40 mt-4">
<img src="./img/CallBack.png" class="h-32 mt-4">

---

## <THeader k="slides.typical_integration.heading" />

``` csharp
 TankEvent = "event:/Tank"
 PunchFX = "event:/Punch"
 //o usar FMODUnity.EventReference para selección en editor
```

### <THeader k="slides.typical_integration.unity_heading" />

```csharp
event = FMODUnity.RuntimeManager.CreateInstance(TankEvent)
event.start();
FMODUnity.RuntimeManager.PlayOneShot(DamageEvent, transform.position);
```

### <THeader k="slides.typical_integration.godot_heading" />

```
event = FmodServer.create_event_instance(TankEvent)
event.start()
FmodServer.play_one_shot(PunchFX)
```

### <THeader k="slides.unreal_integration.heading" />

```c++
UFUNCTION(...)
static FFMODEventInstance PlayEventAtLocation(
  UObject *WorldContextObject,
  UFMODEvent *Event,
  const FTransform &Location,
  bool bAutoPlay );
```

---

# <THeader k="slides.filters_effects.heading" />

<T k="slides.filters_effects.description" />

<img src="./img/TypeOfFilters.png" class="float-right" />

1. <T k="slides.filters_effects.examples.0" />
2. <T k="slides.filters_effects.examples.1" />

---

### <THeader k="slides.volume_control.heading" />

<img src="./img/FMOD_VolumeControl.png" class="h-120">

---

### <THeader k="slides.workflow_recommendations_1.heading" />

<T k="slides.workflow_recommendations_1.description" />
<img src="./img/MusicTable.png">
Source: GDC 18 — Audio Asset Management: Tips and Tricks (Richard Ludlow)
---
## <THeader k="slides.workflow_recommendations_2.heading" />

1) <T k="slides.workflow_recommendations_2.items" />

---

## <THeader k="slides.workflow_recommendations_3.heading" />

1) <T k="slides.workflow_recommendations_3.items" />
<img src="./img/WwiseLauncher.png">

---
## <THeader k="slides.people_work_recommendations_4.heading" />

1) <T k="slides.people_work_recommendations_4.items" />

---
src: ../../slides/closing/questions.md
---

---
src: ../../slides/closing/thank-you.md
---
---
