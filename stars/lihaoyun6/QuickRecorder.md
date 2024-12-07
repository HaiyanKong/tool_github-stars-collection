---
project: QuickRecorder
stars: 4614
description: A lightweight screen recorder based on ScreenCapture Kit for macOS / 基于 ScreenCapture Kit 的轻量化多功能 macOS 录屏工具
url: https://github.com/lihaoyun6/QuickRecorder
---

QuickRecorder
=============

### A lightweight and high-performance screen recorder for macOS  
\[中文版本\]  
\[Landing Page\]

Screenshot
----------

Installation and Usage
----------------------

### System Requirements:

-   macOS 12.3 and Later

### Install:

Download the latest installation file here or install via Homebrew:

brew install lihaoyun6/tap/quickrecorder

### Features/Usage:

-   You can use QuickRecorder to record your screens / windows / applications / mobile devices... etc.
    
-   QuickRecorder supports driver-free audio loopback recording, mouse highlighting, screen magnifier and many more useful features.
    
-   The new **"Presenter Overlay"** in macOS 14 was fully supported by QuickRecorder, which can overlay the camera in real time on your recording _(macOS 12/13 can only use camera floating window)_
    
-   QuickRecorder is able to record `HEVC with Alpha` video format, that can contain alpha channel in the output file _(currently only iMovie and FCPX support this feature)_
    

Q&A
---

**1\. Where can I reopen the main panel after closing it?**

> Click the Dock tile or Menubar icon of QuickRecorder to reopen the main panel at any time.

**2\. Why does QuickRecorder not a sandbox app?**

> QuickRecorder has no plans to be uploaded to the App Store, so it does not need to be designed as a sandbox app.

**3\. How to independently control the volume of system sound and sound from microphone in other video editor?**

> QuickRecorder will merge the audio input from the microphone to the main audio track after recording by default. If you need to edit the video, you can turn off the "Mixdown the track from microphone" option in the settings panel. After turning off, the system sound and sound from microphone will be recorded into two audio tracks and can be edited independently.

Donate
------

Thanks
------

Azayaka @Mnpn

> The source of inspiration and part of the code of the screen recording engine comes from the Azayaka project, and I am also one of the code contributors to this project

KeyboardShortcuts @sindresorhus

> QuickRecorder uses this swift library to handle shortcut key events

SwiftLAME @Hidden Spectrum

> QuickRecorder uses this swift library to handle MP3 output

ChatGPT @OpenAI

> Note: Part of the code in this project was generated or refactored using ChatGPT.
