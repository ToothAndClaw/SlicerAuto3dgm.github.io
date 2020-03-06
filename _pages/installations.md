---
layout: archive
title: "Installations"
permalink: /installations/
author_profile: true
redirect_from:
  - /installations
---

{% include base_path %}

1. Download and Install 3D Slicer: [website](https://download.slicer.org/)
2. Download the `Auto3dgm` module by typing in the terminal: 
```
git clone --recursive https://github.com/ToothAndClaw/auto3dgmSlicerExtension
```
3. Open 3D Slicer and install the required dependencies for `Auto3dgm`. 
Type in the Python interactor: 
```
pip_install("scipy")
pip_install("mosek")
```
4. Manually install `Auto3dgm` module in 3D Slicer.  

    * In 3D Slicer, select Extension Wizard. [image demo](<img src="/images/01.png">)

    * Click *Select Extension* and choose the folder auto3dgmSlicerExtension. [image demo](<img src="/images/02.png">)

    * Click *yes* to load the `Auto3dgm` and the `webviewer` modules. [image demo]( <img src="/images/03.png">)
