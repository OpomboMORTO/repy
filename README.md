![logo](icon/icon.gif "logo")

## About

`repy` is a script to install preconfigured rootfs with [Box86](https://github.com/ptitSeb/box86), [Box64](https://github.com/ptitSeb/box64), [Wine](https://www.winehq.org/) and [DXVK](https://github.com/doitsujin/dxvk) installed. It allows you to run x86 and x86_64 windows programs (such as games) on Android using [Termux](https://github.com/termux/termux-app).

`repy` is not Box64Droid neither Termux-box

## Installation
After installation the start command in termux is `repy`

Download and install
[Termux](https://f-droid.org/repo/com.termux_118.apk),[Termux-X11](https://raw.githubusercontent.com/olegos2/termux-box/main/components/termux-x11-arm64-v8a-debug-latest.apk)

Open termux and paste command

`curl -O https://raw.githubusercontent.com/OpomboMORTO/repy/main/scripts/rootfsEmpty_Install && chmod +x rootfsEmpty_Install && ./rootfsEmpty_Install`

## Configuration
After installation, start the repy environment using the `repy` command, select start to generate a wine prefix, after that go to settings and install directX and the dxvk of your choice.

#
Big thanks to olegos for readme.

## Debugs

* proot environment is slow
  
* creation of the wine prefix and installations of dxvk , directX , is very slow.

* creating the wine container can take 3~5 minutes

## Updates

  `update 23.10.23`

* update 23.10 took a while this last update but it came packed

* added dlls related to audio, fixed audio

* added dma "dynamic allocation memory"

* added dynamics shader, Dynamics wine

* dynamic allocation works by allocating pieces of physical blocks in ram memory, this consumes ram memory, allocating pieces in ram can cause unknown bugs but it is faster, you can only allocate just shaders or the complete wine container, it is not very recommended if you have little memory, the recommendation is at least `8 gigs` to allocate the container

* added wine 17 18 19 20 , ge-proton

* added `wine anti cheate`, it is still being worked on `with lutris-ge` support, it may not work as it should  

* added initial support for `league of legends` in wine anti-creat, if you install directly from the container, don't log in until the installation is complete, several times when opening you may receive a `black screen`

* now when starting up for the first time the prefix installation is automatic, but the installation of dxvk is not, so always after starting go into settings to finish the installation of directX dxvk dx3d8 vkd3d.

* It is possible that when starting x11 it does not start, if this happens close x11 and termux, we do not know the reason, this could be random.

* the bachmarks are broken by the hour

* added bigbox 3 among others  check settings

  `update 19.10.23`

* added turnip support for adrenos 7xx

* added "mesa-23.2.1" "mesa-a7xx"

* removed LLVM for testing

* added maximum gpu clock strength menu "root"

* added force CPU performance mode "root"

* added gallium initial implementation

* added hud menu and advanced menu

* added framebuffer configuration, FB0 required

## Renderers

* Turnip-Zink : for adreno devices from the 6xx line, turnip availability may vary depending on your device, the 7xx line is not compatible in this version
* OpenGl ES : availability for devices with OPENGL-ES support, its compatibility is still being tested, it is only available in opengl 1.X 2.X applications for 3.X 4.X applications use zink


## Third party applications

[Box64](https://github.com/ptitSeb/box64) MIT license

[Box86](https://github.com/ptitSeb/box86) MIT license

[Proot](https://github.com/termux/proot) GPL-2.0 license

[DXVK](https://github.com/doitsujin/dxvk) Zlib license

[DXVK-ASYNC](https://github.com/Sporif/dxvk-async)

[DXVK-GPLASYNC](https://gitlab.com/Ph42oN/dxvk-gplasync)

[VKD3D](https://github.com/lutris/vkd3d) LGPL-2.1 license

[D8VK](https://github.com/AlpyneDreams/d8vk) Zlib license

[Termux-app](https://github.com/termux/termux-app) GPLv3 license

[Termux-x11](https://github.com/termux/termux-x11) GPL-3.0 license

[Wine](https://wiki.winehq.org/Licensing)

[Mesa](https://docs.mesa3d.org/license.html) MIT license

[mesa-zink-11.06.22](https://github.com/alexvorxx/mesa-zink-11.06.22)

[gl4es](https://github.com/ptitSeb/gl4es/tree/master)
MIT license
