# OpenDRT-OCIO-Config
Based on [Jed Smith's repo](https://github.com/jedypod/open-display-transform/) I have created a minimal OCIO config of openDRT 0.3.5 for full CG projects. This is **state-of-the-art Color Management** in its most minimalistic and simple form:
* Inputs (textures) are in "linear"
* Rendering and Nuke working space are also in "linear"
* View Transform is for Rec.1886 display

There is no need to go wide gamut or do anything complex to **craft beautiful images**. Enjoy!

# Image Examples
<p>
    <img ![light_sabers_openDRT_0_3_5] width="192" height="108" src="https://github.com/user-attachments/assets/58ce22fb-5f47-4212-afd4-5de5d64dffc1" >
    <img ![photographic_scene_openDRT_0_3_5] width="192" height="108" src="https://github.com/user-attachments/assets/40a16fe6-cdbc-45a6-815c-03ad226276f9" >
    <img ![lego_sailors_openDRT_0_3_5] width="192" height="108" src="https://github.com/user-attachments/assets/728e804f-c80e-4dfb-97b8-d161ad1e6d2c" >
    <img [louise_concert_openDRT_0_3_5] width="192" height="108" src="https://github.com/user-attachments/assets/75a872d1-09c6-4608-a1c0-b6ed88ef153f" >
    <img ![hue_sweep_openDRT_0_3_5] width="192" height="108" src="https://github.com/user-attachments/assets/7fba91b0-5acf-4ce6-9f96-0874b921f9aa" >  
</p>

Original files (encoded in "linear-AP0") are available [here](https://www.dropbox.com/scl/fo/fhzx0bcwcjylek1oz7kjc/ACGfmi0EHeufVOQPZLvvk7w?rlkey=53cp61955hbns8x46j6cf8k55&e=1&dl=0).

# About the config
* Reference color space is XYZ which is the base of all colourimetry
* "linear" stands for "linear_bt.709"
* "cineonlog_rec709" can be used for a Matte-Painting workflow in Photoshop
* "tlog_egamut" is the Shaper space and can also be used color timing and some log operations in Nuke (such as sharpen)
* An inverse of the View Transform has been provided even though it is not perfect (it was never Jed's goal anyway)
* One may easily add several displays for HDR output if needed (such as P3-D65-PQ)

# Looks
* So far three looks have been added: "Contrast Grade", "Contrast CDL" and "Warmy CDL"
* They have been inspired by the Filmic and AgX OCIO configs (please find links below)
* The use of Looks is highly recommended with Open DRT

## Please note

* Substance_painter roles were set following [this page](https://mrlixm.github.io/blog/substance-painter-color-management/)
* Ideally this config should fit the requirements of [this issue](https://github.com/AcademySoftwareFoundation/OpenColorIO/issues/2011)

# Other available Color Management Workflows
| Name                                                                                             | Author               | Release date |              Observations                             |
|:---:                                                                                             |         :---:        |      :---:   |                 :---:                                 |
| [ARRI K1S1](https://www.arri.com/en/learn-help/learn-help-camera-system/tools/lut-generator)     | Harald Brendel       | 2011         | THE most used LUT on the planet (ARRI Alexa workflow) |
| [Filmic](https://github.com/sobotka/filmic-blender)                                              | Troy Sobotka         | 2017         | Original Blender Color Management Workflow used on [this movie](https://www.youtube.com/watch?v=uf3ALGKgpGU) |
| [RED IPP2](https://support.red.com/hc/en-us/articles/360041467533-RED-LUT-Downloads)             | Graeme Natress       | 2017         | RED Image Processing Pipeline |
| [ACES](https://github.com/AcademySoftwareFoundation/OpenColorIO-Config-ACES/releases)            | AMPAS                | 2021         | Color Encoding System developed by the Academy and used on [this movie](https://www.youtube.com/watch?v=TnGl01FkMMo) |
| [Sony Venice](https://sonycine.com/resources/luts/)                                              | Sony / Picture Shop  | 2022         | LUT files made in partnership with [Picture Shop](https://www.pictureshop.com/) |
| [ARRI Reveal](https://www.arri.com/en/learn-help/learn-help-camera-system/tools/lut-generator)   | Sean Cooper          | 2022         | The new ARRI Alexa35 workflow described [here](https://www.youtube.com/watch?v=s_RXjVeC_7s) |
| [TCAMv3](https://www.filmlight.ltd.uk/support/customer-login/colourspaces/colourspaces.php)      | Daniele Siragusano   | 2024         | Baselight Color Management Workflow explained [here](https://youtu.be/DL4n6LErMbw?t=325) |
| [AgX Blender](https://github.com/EaryChow/AgX)                                                   | Eary Chow            | 2023         | New Blender Color Management Workflow used on [this video game](https://www.youtube.com/watch?v=mVjBRZqajYY) |
| [AgX SB2383](https://github.com/sobotka/SB2383-Configuration)                                    | Troy Sobotka         | 2024         | Minimal AgX OCIO Config using Linear BT.709 |
| [JP-2499](https://github.com/jedypod/JP2499)                                                     | Juan Pablo Zambrano  | 2024         | A very popular picture formation pipeline described [here](https://www.liftgammagain.com/forum/index.php?threads/2499-drt-an-alternative-picture-formation-pipeline.18639/) |
