---
layout: archive
title: "Installations"
permalink: /installations/
author_profile: true
redirect_from:
  - /installations
---

{% include base_path %}

Download and Install 3D Slicer: [https://download.slicer.org/](https://download.slicer.org/)

## Install `Auto3dgm` extension via Extension Manager in Slicer

1. Open 3D Slicer and install the required denpendencis for `Auto3dgm`.
Type in the Python interactor:
```
pip_install("mosek")
```

2. In 3D Slicer, go to `View->Extension Manager`. [image demo](<img src="/images/em.\
png">)
 
3. In the "Install Extensions" tab, select `Auto3dgm` extension, and click on "Install".

4. After the extension is installed, restart slicer. The `Auto3dgm` extension is available to use. 

For more information on how to install an extension using the Extension Manager in Slicer, please visit [https://bit.ly/SlicerExtensionManager](https://www.slicer.org/wiki/Documentation/4.3/SlicerApplication/ExtensionsManager#Installing_an_extension)

## Install `Auto3dgm` beta version from source code

1. Open a terminal and type the following to download the `Auto3dgm` beta version: 
```
git clone --recursive https://github.com/ToothAndClaw/auto3dgmSlicerExtension
```
2. Open 3D Slicer and install the required dependencies for `Auto3dgm`. 
Type in the Python interactor: 
```
pip_install("mosek")
```
3. Manually install `Auto3dgm` module in 3D Slicer.  

    * In 3D Slicer, select Extension Wizard. [image demo](<img src="/images/01.png">)

    * Click *Select Extension* and choose the folder auto3dgmSlicerExtension. [image demo](<img src="/images/02.png">)

    * Click *yes* to load the `Auto3dgm` and the `webviewer` modules. [image demo]( <img src="/images/03.png">)
