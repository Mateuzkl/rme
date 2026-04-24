What is this?
=============

This is a map editor for OpenTibia, which is an open source implementation of the MMORPG Tibia (which can be found at [tibia.com](http://tibia.com)), the official website is [remeresmapeditor.com](http://remeresmapeditor.com).
You can find the project for hosting your own server at [the otserv project](https://github.com/opentibia/server).
The main fansite for help, discussion and servers is [otland.net](http://otland.net).

I want to contribute
====================

Contributions are very welcome, if you would like to make any changes, fork this project or request commit access.
I (Remere) am liberal to allowing any and all help and my involvement will be restricted to reviewing changes for now.
Please, if you would like to contribute anything, documentation, extensions or code speak up!

Bugs
======

Have you found a bug? Please create an issue in our [bug tracker](https://github.com/hjnilsson/rme/issues)

Other Applications
==========

* To host your MMORPG game server, you can use [The Forgotten Server](https://github.com/otland/forgottenserver).
* To play your MMORPG game, you can use [OTClient](https://github.com/edubart/otclient)
* To map your MMORPG game, you can use this map editor.

Download
========

You can find official releases at [remeres mapeditor website](http://remeresmapeditor.com/marklar.php).

If you are looking for the 3.X version, download it [here](https://github.com/hjnilsson/rme/releases/) until It is added to the official website.

Compiling
=========

## Windows

Before building RME on Windows, you must install and configure vcpkg first.

### Why this is required:

This project now uses a `vcpkg.json` manifest file. That file declares the external libraries the project depends on. When Visual Studio detects the vcpkg manifest integration, it can automatically resolve, download, and install any missing dependencies required by the solution.

In other words:
- `vcpkg.json` tells the project which packages are required
- vcpkg manages those packages for you
- if a dependency is missing, vcpkg can fetch and install it automatically
- this avoids manual library setup and keeps the build environment consistent

### Setup steps on Windows:

```bash
git clone https://github.com/microsoft/vcpkg.git
cd vcpkg
.\bootstrap-vcpkg.bat
.\vcpkg.exe integrate install
```

**Important:**
You must run each command exactly as shown. The `integrate install` step is required so Visual Studio can detect vcpkg automatically when opening the solution.

### After that:

Open `\rme\vcproj\RME.sln` in Visual Studio 2022, then click Build Solution and wait until the compilation finishes successfully.

**Requirement:**
Visual Studio 2022 is required to build the project.

---

## Other Platforms

Required libraries:
* wxWidgets >= 3.0
* Boost >= 1.66.0
* fmt
* nlohmann-json
* OpenGL
* FreeGLUT
* zlib

[Compile on Ubuntu](https://github.com/hjnilsson/rme/wiki/Compiling-on-Ubuntu)

[Compile on Arch Linux](https://github.com/hjnilsson/rme/wiki/Compiling-on-Arch-Linux)

[Compile on macOS](https://github.com/hjnilsson/rme/wiki/Compiling-on-macOS)
