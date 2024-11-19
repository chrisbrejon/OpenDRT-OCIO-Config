# OpenDRT-OCIO-Config
Based on Jed Smith's repo https://github.com/jedypod/open-display-transform/ I wanted to create a minimal OCIO config of openDRT 0.3.5 for full CG projects.

This is state-of-the-art / cutting-edge Color Management but in its most minimalistic and simple form.

I don't think you can do a config more "plug and play play" than this one:
- Inputs (textures) are in "linear"
- Rendering and Nuke working space are also in "linear"
- View Transform is for Rec.1886 display

There is no need to go wide gamut or anything complex to make your images look great. Enjoy !

![light_sabers_openDRT_0_3_5](https://github.com/user-attachments/assets/2ab46d1b-6f09-4159-a771-f5659ae789fc)
![photographic_scene_openDRT_0_3_5](https://github.com/user-attachments/assets/40a16fe6-cdbc-45a6-815c-03ad226276f9)
![lego_sailors_openDRT_0_3_5](https://github.com/user-attachments/assets/271591b9-d83b-4eb4-aa6e-df0fb0601aac)
![louise_concert_openDRT_0_3_5](https://github.com/user-attachments/assets/75a872d1-09c6-4608-a1c0-b6ed88ef153f)

For those curious out there, a few things about the config:
- Reference color space is XYZ which is the base of all colourimetry
- One may add easily colorspaces such as ACEScg or ACES2065-1 if needed
- One also may add several displays for HDR output if needed (such as P3 D65 PQ)

But I didn't do such thing because my goal was to provide a simple OCIOv1 config in its most essential form.

