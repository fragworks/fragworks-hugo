---
date: 2017-04-13T00:01:53-04:00
title: Framework for Rather Awesome Games
type: homepage
menu: main
weight: 0
markup: "rst"
---

Introduction
============

**FRAG** is a cross-platform 2D (eventually 3D) game creation framework for the Nim programming language.
It is still very early in its development lifecycle so if you decide to use it, please understand it will be rough around the edges.
Please also note that this documentation may be incomplete and or may rapidly change.

Dependencies
============

- `Nim <https://github.com/nim-lang/Nim.git>`_
- `Nimble <https://github.com/nim-lang/nimble>`_
- `GENie <https://github.com/bkaradzic/GENie>`_
- `SDL2 <https://www.libsdl.org/download-2.0.php>`_
- `SDL_image <https://www.libsdl.org/projects/SDL_image/>`_

Instructions for building and installing the above listed dependencies, are outside of the scope of this document.

Installation Instructions
=========================

1. Clone the project from its `Github repository <https://github.com/fragworks/frag>`_:

.. code-block:: bash

  $ git clone https://github.com/fragworks/frag.git && cd frag

2. Clone and update submodules:

.. code-block:: bash
  
  $ git submodule update --init vendor/bx vendor/bgfx vendor/bimg

Note: Android and Chipmunk2D support are both optional and very experimental. If desired, add `platforms/android` and | or `vendor/Chipmunk2D` to the list of submodules respectively.

3. Install Nim dependencies via nimble:

.. code-block:: bash

  $ nimble install -y

4. Run the nake command to get a list of operating systems and architectures framework dependencies can be built for:

.. code-block:: bash

  $ nake

   Available tasks:
   android-arm-debug32 - Build debug versions of FRAG dependencies for ARM 32-bit instruction set
   linux-debug32 - Build debug verisons of FRAG dependencies for Linux 32-bit instruction set
   linux-debug64 - Build debug verisons of FRAG dependencies for Linux 64-bit instruction set
   osx-debug32 - Build debug verisons of FRAG dependencies for OSX 32-bit instruction set
   osx-debug64 - Build debug verisons of FRAG dependencies for OSX 64-bit instruction set
   osx-release32 - Build release verisons of FRAG dependencies for OSX 32-bit instruction set
   osx-release64 - Build release verisons of FRAG dependencies for OSX 64-bit instruction set
   win-debug32 - Build debug verisons of FRAG dependencies for Windows 32-bit instruction set
   win-debug64 - Build debug verisons of FRAG dependencies for Windows 64-bit instruction set
   win-release32 - Build debug verisons of FRAG dependencies for Windows 32-bit instruction set
   win-release64 - Build debug verisons of FRAG dependencies for Windows 64-bit instruction set

5. Run the appropriate nake task(s) depending on the operating system and architecture you plan on targeting for your project:

.. code-block:: bash

  $ nake osx-release64

Examples
========

**FRAG** ships with a number of examples which serve a dual purpose:

1. System tests for the framework.
2. Examples of framework features.

These examples don't necessarily exhibit best practices for using the framework. Refer to the `Samples <#samples>`_ section .

To get a list of examples simply run the nake command in the `examples` directory:

.. code-block:: bash

  $ cd examples && nake

   Available tasks:
   D00 - Desktop : Run example hello-world
   D01 - Desktop : Run example sprite-batch
   D02 - Desktop : Run example audio
   D03 - Desktop : Run example input
   D04 - Desktop : Run example sprite-animation
   D05 - Desktop : Run example gui
   D06 - Desktop : Run example physics
   A00 - Android : Run example hello-world

Then run the appropriate nake task for the example you would like to run, ex:

.. code-block:: bash

  $ nake D00

Samples
=======

Samples are currently in development. As they are finished, instructions for installing and running them will appear here.