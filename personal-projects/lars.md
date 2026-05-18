---
layout: single 
title: "LARS"
author_profile: true 
classes: wide
---
LARS stands for Live Asr (automatic speech recognition) with Raspberry pi S. Which is not a good acronym, but I like LARS as a project name so I have stuck with it. While I like the project name it is no longer completely accurate to the project, initially the plan was to run ASR locally on a Raspberry Pi, but I lost interest in that.

The current project architecture is described in the figure shown here:

<div style="max-width:1000px; margin:0 auto; padding:20px;">
  <img src="/assets/images/lars/refactor_structure.png" alt="LARS Refactor Structure">
</div>

All of the code for speech detection/logic is now hosted on a central server (my old desktop sitting in my closet) with the microphones connected directly to it. All of the execution before "Real World Action" is exectued on this server. The "Real World Action" can describes many things, but currently it is an IOT style Raspberry Pi setup that controls relays.

The repo for the code can be found [here](https://github.com/dylenthomas/LiveASRonRPi-4)