# OpenDRT-OCIO-Config
Based on [Jed Smith's repo](https://github.com/jedypod/open-display-transform/) I have created a minimal OCIO config of openDRT 0.3.5 for full CG projects.

This is state-of-the-art Color Management in its most minimalistic and simple form:
* Inputs (textures) are in "linear"
* Rendering and Nuke working space are also in "linear"
* View Transform is for Rec.1886 display

There is no need to go wide gamut or do anything complex to craft beautiful images. Enjoy!

![light_sabers_openDRT_0_3_5](https://github.com/user-attachments/assets/2ab46d1b-6f09-4159-a771-f5659ae789fc)
![photographic_scene_openDRT_0_3_5](https://github.com/user-attachments/assets/40a16fe6-cdbc-45a6-815c-03ad226276f9)
![lego_sailors_openDRT_0_3_5](https://github.com/user-attachments/assets/271591b9-d83b-4eb4-aa6e-df0fb0601aac)
![louise_concert_openDRT_0_3_5](https://github.com/user-attachments/assets/75a872d1-09c6-4608-a1c0-b6ed88ef153f)

For those curious out there, a few things about the config:
* Reference color space is XYZ which is the base of all colourimetry
* "linear" stands for "linear-bt.709"
* An inverse of the View Transform has been provided even though it is not perfect (it was never Jed's goal anyway)
* One may easily add several displays for HDR output if needed (such as P3-D65-PQ)

Please note:

* Substance_painter roles were set following [this page](https://mrlixm.github.io/blog/substance-painter-color-management/)
* Ideally this config should fit the requirements of [this issue](https://github.com/AcademySoftwareFoundation/OpenColorIO/issues/2011)

Other Color Management Workflows are available here:
| Name | Author | Release date |
|:---: |  :---: |      :---:   |
| [ARRI K1S1](https://www.arri.com/en/learn-help/learn-help-camera-system/tools/lut-generator)     | Harald Brendel       | 2011    |
| [Filmic](https://github.com/sobotka/filmic-blender)                                              | Troy Sobotka         | 2017    |
| [RED IPP2](https://support.red.com/hc/en-us/articles/360041467533-RED-LUT-Downloads)             | Graeme Natress       | 2017    |
| [ACES](https://github.com/AcademySoftwareFoundation/OpenColorIO-Config-ACES/releases)            | AMPAS                | 2021    |
| [Sony Venice](https://sonycine.com/resources/luts/)                                              | Sony / Picture Shop  | 2022    |
| [ARRI Reveal](https://www.arri.com/en/learn-help/learn-help-camera-system/tools/lut-generator)   | Sean Cooper          | 2022    |
| [TCAMv3](https://www.filmlight.ltd.uk/support/customer-login/colourspaces/colourspaces.php)      | Daniele Siragusano   | 2024    |
| [AgX Blender](https://github.com/EaryChow/AgX)                                                   | Eary Chow            | 2023    |
| [AgX SB2383](https://github.com/sobotka/SB2383-Configuration)                                    | Troy Sobotka         | 2024    |
| [JP-2499](https://github.com/JuanPabloZambrano/DCTL/tree/main/2499_DRT/JP-2499DRT%20OCIO)        | Juan Pablo Zambrano  | 2024    |
