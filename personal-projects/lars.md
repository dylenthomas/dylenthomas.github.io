---
layout: single 
title: "LARS"
author_profile: true 
---
LARS stands for Live Asr (automatic speech recognition) with Raspberry pi S. Which is not a good acronym, but I like LARS as a project name so I have stuck with it.
Also it is no longer completely accurate to the project, initially the plan was to run ASR locally on a Raspberry Pi, but I lost interest in that.
So, now the ASR is done on my desktop server which acts as a "compute node", and when it detects any keywords I have defined, it communicates with the edge device, which is a Raspberry Pi.
The Raspberry Pi then executes a command corresponding to the keyword, such as turning the lights in my room off/on.
The compute node gets audio from two microphones I have setup on the walls of my room, and it commuicates with the Raspberry Pi over TCP.

The repo for the code can be found [here](https://github.com/dylenthomas/LiveASRonRPi-4)

{% assign lars_projects = site.posts | where_exp:"post","post.tags contains 'LARS'" %}
{% for project in lars_projects %}
### [{{ project.title }}]({{ project.url }})
{{ project.excerpt }}
{% endfor %}

