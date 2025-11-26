# OpenDRT-OCIO-Config
Based on [Jed Smith's repo](https://github.com/jedypod/open-display-transform/) I have created a minimal OCIO config of openDRT 1.0.0 for full CG projects. This is **state-of-the-art Color Management** in its most minimalistic and simple form:
* Inputs (textures) are in "linear"
* Rendering and Nuke working space are also in "linear"
* View Transform is for Rec.1886 display

There is no need to go wide gamut or do anything complex to **craft beautiful images**. Enjoy!

# Image Examples
<p>
    <img ![hue_sweep_openDRT_1_0_0] width="144" height="81" src="https://github.com/user-attachments/assets/47f8e0b4-5e06-4d61-ab6a-15e1cfbd4b90" >  
    <img ![photographic_scene_openDRT_1_0_0] width="144" height="81" src="https://github.com/user-attachments/assets/960c7c5d-fc0c-4802-b78f-8d31ffd5dd35" >
    <img ![light_sabers_openDRT_1_0_0] width="144" height="81" src="https://github.com/user-attachments/assets/cc483018-0fd1-459a-bb82-0d34b61df2fe" >
    <img ![lego_sailors_openDRT_1_0_0] width="144" height="81" src="https://github.com/user-attachments/assets/1855d01a-3f8b-4bc3-88de-0921eeb8aec3" >
    <img ![louise_concert_openDRT_1_0_0] width="144" height="81" src="https://github.com/user-attachments/assets/7f0784da-d972-4b5e-b62a-9a10dd1bec95" >
</p>

Original files (encoded in "linear-AP0") are available [here](https://www.dropbox.com/scl/fo/fhzx0bcwcjylek1oz7kjc/ACGfmi0EHeufVOQPZLvvk7w?rlkey=53cp61955hbns8x46j6cf8k55&e=1&dl=0).

# About the config
* Reference color space is XYZ which is the base of all colourimetry
* All matrixes have been generated using [colour-science](https://www.colour-science.org/apps/) with "CIE XYZ-D65 - Scene-referred" and "CAT02"
* "linear" stands for "linear_bt.709"
* "cineonlog_rec709" can be used for a matte-painting workflow in Photoshop
* "tlog_egamut" is the shaper space. It can be used for color timing and some log operations (such as sharpen)
* Substance_painter roles were set following [this page](https://mrlixm.github.io/blog/substance-painter-color-management/)
* An inverse of the View Transform has been provided even though it is not perfect
* One may easily add several colorspaces or displays for HDR output if needed (such as "p3_d65_pq")

# Looks
* So far two looks have been added: "Contrast CDL" and "Warmy CDL"
* They have been inspired by the Filmic and AgX OCIO configs (please find links below)
* The use of Looks is highly recommended with Open DRT
* To use one of the looks, you need to combine it with a View. Like this for instance:

```- !<View> {name: OpenDRT 1.0.0 Contrast, colorspace: openDRT 1.0.0 - Rec.709 - 2.4 Gamma, looks: Contrast CDL}```

# Other available Color Management Workflows
| Name                                                                                             | Author               | Release date |              Observations                             |
|:---:                                                                                             |         :---:        |      :---:   |                 :---:                                 |
| [ARRI K1S1](https://www.arri.com/en/learn-help/learn-help-camera-system/tools/lut-generator)     | Harald Brendel       | 2011         | THE most used LUT on the planet (ARRI Alexa workflow) |
| [ACES](https://github.com/AcademySoftwareFoundation/OpenColorIO-Config-ACES/releases)            | AMPAS                | 2016         | Color Encoding System developed by the Academy |
| [Filmic](https://github.com/sobotka/filmic-blender)                                              | Troy Sobotka         | 2017         | Original Blender Color Management used on [this movie](https://www.youtube.com/watch?v=uf3ALGKgpGU) |
| [RED IPP2](https://support.red.com/hc/en-us/articles/360041467533-RED-LUT-Downloads)             | Graeme Natress       | 2017         | RED Image Processing Pipeline explained [here](https://www.red.com/red-tech/image-processing-pipeline-ipp2) |
| [Sony Venice](https://sonycine.com/resources/luts/)                                              | Sony / Picture Shop  | 2022         | LUT files made in partnership with [Picture Shop](https://www.pictureshop.com/) |
| [ARRI Reveal](https://www.arri.com/en/learn-help/learn-help-camera-system/tools/lut-generator)   | Sean Cooper          | 2022         | The new ARRI Alexa35 workflow described [here](https://www.youtube.com/watch?v=s_RXjVeC_7s) |
| [Tony](https://github.com/h3r2tic/tony-mc-mapface)                                     | Tomasz Stachowiak    | 2023         | A cool-headed display transform |
| [AgX Blender](https://github.com/EaryChow/AgX)                                                   | Eary Chow            | 2023         | Blender Color Management used on [this video game](https://www.youtube.com/watch?v=mVjBRZqajYY) |
| [TCAMv3](https://www.filmlight.ltd.uk/support/customer-login/colourspaces/colourspaces.php)      | Daniele Siragusano   | 2024         | Baselight Color Management Workflow explained [here](https://youtu.be/DL4n6LErMbw?t=325) |
| [AgX SB2383](https://github.com/sobotka/SB2383-Configuration)                                    | Troy Sobotka         | 2024         | Minimal AgX OCIO Config using Linear BT.709 |
| [JP-2499](https://github.com/jedypod/JP2499)                                                     | JP Zambrano          | 2024         | A popular picture formation pipeline described [here](https://www.liftgammagain.com/forum/index.php?threads/2499-drt-an-alternative-picture-formation-pipeline.18639/) |
